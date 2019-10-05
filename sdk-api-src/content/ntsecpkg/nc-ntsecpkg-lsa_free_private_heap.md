---
UID: NC:ntsecpkg.LSA_FREE_PRIVATE_HEAP
title: LSA_FREE_PRIVATE_HEAP (ntsecpkg.h)
author: windows-sdk-content
description: Frees memory that was allocated by using the AllocatePrivateHeap function.
old-location: security\freeprivateheap.htm
tech.root: SecAuthN
ms.assetid: f1ca1450-c59c-4c0f-b68b-373f1a7c70da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreePrivateHeap, FreePrivateHeap callback function [Security], LSA_FREE_PRIVATE_HEAP, LSA_FREE_PRIVATE_HEAP callback, ntsecpkg/FreePrivateHeap, security.freeprivateheap
ms.topic: callback
f1_keywords:
- ntsecpkg/FreePrivateHeap
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
- FreePrivateHeap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_FREE_PRIVATE_HEAP callback function


## -description


Frees memory that was allocated by using the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_private_heap">AllocatePrivateHeap</a> function.


## -parameters




### -param Base [in]

A pointer to the memory to be freed.


## -returns



This callback function does not return a value.




## -remarks



A pointer to the <b>FreePrivateHeap</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

