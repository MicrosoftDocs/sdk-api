---
UID: NC:ntsecpkg.LSA_CREATE_SHARED_MEMORY
title: LSA_CREATE_SHARED_MEMORY (ntsecpkg.h)
author: windows-sdk-content
description: The CreateSharedMemory function creates a section of memory that is shared by client processes and the security package.
old-location: security\createsharedmemory.htm
tech.root: SecAuthN
ms.assetid: 22abafd7-1648-4bea-a0a8-0cb58333fbea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSharedMemory, CreateSharedMemory callback function [Security], LSA_CREATE_SHARED_MEMORY, LSA_CREATE_SHARED_MEMORY callback, _ssp_createsharedmemory, ntsecpkg/CreateSharedMemory, security.createsharedmemory
ms.topic: callback
f1_keywords:
- ntsecpkg/CreateSharedMemory
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
- CreateSharedMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_CREATE_SHARED_MEMORY callback function


## -description


The <b>CreateSharedMemory</b> function creates a section of memory that is shared by client processes and the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a>.


## -parameters




### -param MaxSize [in]

Specifies the maximum size of the shared memory.


### -param InitialSize [in]

Specifies the initial size of the shared memory.


## -returns



The function returns a pointer to the block of shared memory, or <b>NULL</b> if the block was not reserved.




## -remarks



Creating a shared section for each client is not advisable because it is a resource-intensive operation and may exhaust system resources.

The package's clients can write to shared memory which makes it susceptible to attack. Data in the shared segment should not be trusted.

The pointer returned by the <b>CreateSharedMemory</b> function is required by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_shared_memory">DeleteSharedMemory</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a> functions.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_shared_memory">DeleteSharedMemory</a> function to release memory reserved by the <b>CreateSharedMemory</b> function.

Pointers to these functions are available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory">AllocateSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_shared_memory">DeleteSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

