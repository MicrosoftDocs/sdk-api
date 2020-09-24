---
UID: NC:ntsecpkg.LSA_FREE_PRIVATE_HEAP
title: LSA_FREE_PRIVATE_HEAP (ntsecpkg.h)
description: Frees memory that was allocated by using the AllocatePrivateHeap function.
helpviewer_keywords: ["FreePrivateHeap","FreePrivateHeap callback function [Security]","LSA_FREE_PRIVATE_HEAP","LSA_FREE_PRIVATE_HEAP callback","ntsecpkg/FreePrivateHeap","security.freeprivateheap"]
old-location: security\freeprivateheap.htm
tech.root: security
ms.assetid: f1ca1450-c59c-4c0f-b68b-373f1a7c70da
ms.date: 12/05/2018
ms.keywords: FreePrivateHeap, FreePrivateHeap callback function [Security], LSA_FREE_PRIVATE_HEAP, LSA_FREE_PRIVATE_HEAP callback, ntsecpkg/FreePrivateHeap, security.freeprivateheap
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
 - LSA_FREE_PRIVATE_HEAP
 - ntsecpkg/LSA_FREE_PRIVATE_HEAP
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
 - FreePrivateHeap
---

# LSA_FREE_PRIVATE_HEAP callback function


## -description

Frees memory that was allocated by using the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_private_heap">AllocatePrivateHeap</a> function.

## -parameters

### -param Base [in]

A pointer to the memory to be freed.

## -remarks

A pointer to the <b>FreePrivateHeap</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>