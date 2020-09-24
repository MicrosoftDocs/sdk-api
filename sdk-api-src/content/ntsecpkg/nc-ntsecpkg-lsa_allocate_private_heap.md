---
UID: NC:ntsecpkg.LSA_ALLOCATE_PRIVATE_HEAP
title: LSA_ALLOCATE_PRIVATE_HEAP (ntsecpkg.h)
description: Allocates memory on the private heap.
helpviewer_keywords: ["AllocatePrivateHeap","AllocatePrivateHeap callback function [Security]","LSA_ALLOCATE_PRIVATE_HEAP","LSA_ALLOCATE_PRIVATE_HEAP callback","ntsecpkg/AllocatePrivateHeap","security.allocateprivateheap"]
old-location: security\allocateprivateheap.htm
tech.root: security
ms.assetid: 956e7aaf-e8b3-4db5-945a-b579f946b769
ms.date: 12/05/2018
ms.keywords: AllocatePrivateHeap, AllocatePrivateHeap callback function [Security], LSA_ALLOCATE_PRIVATE_HEAP, LSA_ALLOCATE_PRIVATE_HEAP callback, ntsecpkg/AllocatePrivateHeap, security.allocateprivateheap
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
 - LSA_ALLOCATE_PRIVATE_HEAP
 - ntsecpkg/LSA_ALLOCATE_PRIVATE_HEAP
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
 - AllocatePrivateHeap
---

# LSA_ALLOCATE_PRIVATE_HEAP callback function


## -description

Allocates memory on the private heap.

Memory allocated with this routine must be deallocated with the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_free_private_heap">FreePrivateHeap</a> function.

## -parameters

### -param Length [in]

Number of bytes to allocate from the heap.

## -returns

This function returns a pointer to the allocated heap memory. If memory could not be allocated, the function returns <b>NULL</b>.

## -remarks

A pointer to the <b>AllocatePrivateHeap</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>