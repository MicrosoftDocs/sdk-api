---
UID: NC:ntsecpkg.LSA_DELETE_SHARED_MEMORY
title: LSA_DELETE_SHARED_MEMORY (ntsecpkg.h)
description: The DeleteSharedMemory function releases a section of memory that is shared by clients and a security package.helpviewer_keywords: ["DeleteSharedMemory","DeleteSharedMemory callback function [Security]","LSA_DELETE_SHARED_MEMORY","LSA_DELETE_SHARED_MEMORY callback","_ssp_deletesharedmemory","ntsecpkg/DeleteSharedMemory","security.deletesharedmemory"]
old-location: security\deletesharedmemory.htm
tech.root: SecAuthN
ms.assetid: 8059ff30-6301-4cf6-9620-2ba765303bb4
ms.date: 12/05/2018
ms.keywords: DeleteSharedMemory, DeleteSharedMemory callback function [Security], LSA_DELETE_SHARED_MEMORY, LSA_DELETE_SHARED_MEMORY callback, _ssp_deletesharedmemory, ntsecpkg/DeleteSharedMemory, security.deletesharedmemory
f1_keywords:
- ntsecpkg/DeleteSharedMemory
dev_langs:
- c++
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- DeleteSharedMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_DELETE_SHARED_MEMORY callback function


## -description


The <b>DeleteSharedMemory</b> function releases a section of memory that is shared by clients and a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a>.


## -parameters




### -param SharedMem [in]

Pointer to shared memory previously reserved by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



The <b>DeleteSharedMemory</b> function releases the shared memory reserved by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a> function.

To release shared memory allocated by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a> function, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a> function.

Pointers to these functions are available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

