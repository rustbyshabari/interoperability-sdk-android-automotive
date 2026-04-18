# BHILANI Interoperability by kantini, chanchali

Run SDK

    Android Studio

Usage

    import kotlinx.coroutines.Dispatchers
    import kotlinx.coroutines.withContext
    import rust.interop.bridge.*
    
    // Pure logic to fetch data from the Rust JNI bridge
    suspend fun fetchDataFromRust(pageNumber: Int): FilterResponse {
    
        // 1. Create the params object
        val params = FilterParams(
            language = null,
            integration = null,
            crates = null,
            developmentkit = null,
            page = pageNumber.toString(),
            ids = null
        )
    
        // 2. Execute the call on the IO thread
        return withContext(Dispatchers.IO) {
            fetchInteroperability(params)
        }        
    }

Screenshot (Page 1)
<img width="1080" height="600" alt="aaos1" src="https://github.com/user-attachments/assets/7b674202-bc4b-4e2b-a194-b60817b90660" />

Screenshot (Page 4)
<img width="1080" height="600" alt="aaos2" src="https://github.com/user-attachments/assets/edb50c96-0e0c-46ce-a609-d407f0c6c0be" />

**@AIAmitSuri, Co-creator/Co-founder (🙏 Mata Shabri 🙏)**
