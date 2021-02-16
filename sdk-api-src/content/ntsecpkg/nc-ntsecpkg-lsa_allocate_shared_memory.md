---
UID: NC:ntsecpkg.LSA_ALLOCATE_SHARED_MEMORY
title: LSA_ALLOCATE_SHARED_MEMORY (ntsecpkg.h)
description: The AllocateSharedMemory function allocates a block of shared memory from a section of memory previously reserved by a call to the CreateSharedMemory function.
helpviewer_keywords: ["AllocateSharedMemory","AllocateSharedMemory callback function [Security]","LSA_ALLOCATE_SHARED_MEMORY","LSA_ALLOCATE_SHARED_MEMORY callback","_ssp_allocatesharedmemory","ntsecpkg/AllocateSharedMemory","security.allocatesharedmemory"]
old-location: security\allocatesharedmemory.htm
tech.root: security
ms.assetid: 77fdedaf-8931-4412-ab35-bd3de8e78b9a
ms.date: 12/05/2018
ms.keywords: AllocateSharedMemory, AllocateSharedMemory callback function [Security], LSA_ALLOCATE_SHARED_MEMORY, LSA_ALLOCATE_SHARED_MEMORY callback, _ssp_allocatesharedmemory, ntsecpkg/AllocateSharedMemory, security.allocatesharedmemory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_ALLOCATE_SHARED_MEMORY
 - ntsecpkg/LSA_ALLOCATE_SHARED_MEMORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - AllocateSharedMemory
---

# LSA_ALLOCATE_SHARED_MEMORY callback function


## -description

The <b>AllocateSharedMemory</b> function allocates a block of shared memory from a section of memory previously reserved by a call to the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a> function.

## -parameters

### -param SharedMem [in]

Pointer to a section of reserved shared memory.

### -param Size [in]

Specifies the amount of shared memory to allocate, in bytes.

## -returns

If the function succeeds, the return value is a pointer to the allocated memory.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Reserve a section of shared memory using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a> function. Free a block of memory allocated by <b>AllocateSharedMemory</b> using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a> function.

A pointer to the <b>AllocateSharedMemory</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory">CreateSharedMemory</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory">FreeSharedMemory</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>