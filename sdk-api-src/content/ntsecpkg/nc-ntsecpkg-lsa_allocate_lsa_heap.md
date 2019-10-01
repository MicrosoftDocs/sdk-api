---
UID: NC:ntsecpkg.LSA_ALLOCATE_LSA_HEAP
title: LSA_ALLOCATE_LSA_HEAP (ntsecpkg.h)
author: windows-sdk-content
description: Allocates memory on the heap. Some information passed back to the LSA is expected to be allocated using this function.
old-location: security\allocatelsaheap.htm
tech.root: SecAuthN
ms.assetid: cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllocateLsaHeap, AllocateLsaHeap callback function [Security], LSA_ALLOCATE_LSA_HEAP, LSA_ALLOCATE_LSA_HEAP callback, _lsa_allocatelsaheap, ntsecpkg/AllocateLsaHeap, security.allocatelsaheap
ms.topic: callback
f1_keywords:
- ntsecpkg/AllocateLsaHeap
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
- AllocateLsaHeap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_ALLOCATE_LSA_HEAP callback function


## -description


Allocates memory on the heap. Some information passed back to the LSA is expected to be allocated using this function. Memory allocated with this routine must be deallocated with the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap">FreeLsaHeap</a> function.
			
		


## -parameters




### -param Length [in]

Number of bytes to allocate from the heap.


## -returns



This function returns a pointer to the allocated heap memory. If memory could not be allocated, the function returns <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

