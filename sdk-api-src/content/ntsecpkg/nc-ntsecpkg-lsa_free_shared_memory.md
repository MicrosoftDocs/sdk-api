---
UID: NC:ntsecpkg.LSA_FREE_SHARED_MEMORY
title: LSA_FREE_SHARED_MEMORY (ntsecpkg.h)
author: windows-sdk-content
description: The FreeSharedMemory function frees a block of shared memory previously allocated by the AllocateSharedMemory function.
old-location: security\freesharedmemory.htm
tech.root: SecAuthN
ms.assetid: def16ef0-4ae7-43c5-99c8-493bdf0c6a97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeSharedMemory, FreeSharedMemory callback function [Security], LSA_FREE_SHARED_MEMORY, LSA_FREE_SHARED_MEMORY callback, _ssp_freesharedmemory, ntsecpkg/FreeSharedMemory, security.freesharedmemory
ms.topic: callback
f1_keywords:
- ntsecpkg/FreeSharedMemory
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
- FreeSharedMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_FREE_SHARED_MEMORY callback function


## -description


The <b>FreeSharedMemory</b> function frees a block of shared memory previously allocated by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a> function.


## -parameters




### -param SharedMem [in]

Pointer to the shared memory section previously reserved using the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a> function.


### -param Memory [in]

Pointer to the memory previously allocated from the shared memory section specified by the <i>SharedMem</i> parameter, using the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a> function.


## -returns



This function does not return a value.




## -remarks



A pointer to the <b>FreeSharedMemory</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

