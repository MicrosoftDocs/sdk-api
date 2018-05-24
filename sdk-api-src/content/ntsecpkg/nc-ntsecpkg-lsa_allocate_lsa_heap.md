---
UID: NC:ntsecpkg.LSA_ALLOCATE_LSA_HEAP
title: LSA_ALLOCATE_LSA_HEAP
author: windows-driver-content
description: Allocates memory on the heap. Some information passed back to the LSA is expected to be allocated using this function.
old-location: security\allocatelsaheap.htm
old-project: SecAuthN
ms.assetid: cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: AllocateLsaHeap, AllocateLsaHeap function [Security], LSA_ALLOCATE_LSA_HEAP, _lsa_allocatelsaheap, ntsecpkg/AllocateLsaHeap, security.allocatelsaheap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	AllocateLsaHeap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_ALLOCATE_LSA_HEAP callback function


## -description


Allocates memory on the heap. Some information passed back to the LSA is expected to be allocated using this function. Memory allocated with this routine must be deallocated with the 
<a href="https://msdn.microsoft.com/bd461a23-2501-48c5-8f2f-c6c98383157f">FreeLsaHeap</a> function.
			
		


## -parameters




### -param Length [in]

Number of bytes to allocate from the heap.


## -returns



This function returns a pointer to the allocated heap memory. If memory could not be allocated, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

