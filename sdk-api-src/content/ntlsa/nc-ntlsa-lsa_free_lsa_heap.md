---
UID: NC:ntlsa.LSA_FREE_LSA_HEAP
title: LSA_FREE_LSA_HEAP (ntlsa.h)
description: Deallocates heap memory previously allocated by AllocateLsaHeap.
helpviewer_keywords: ["FreeLsaHeap","FreeLsaHeap callback function [Security]","LSA_FREE_LSA_HEAP","LSA_FREE_LSA_HEAP callback","_lsa_freelsaheap","ntlsa/FreeLsaHeap","security.freelsaheap"]
old-location: security\freelsaheap.htm
tech.root: security
ms.assetid: bd461a23-2501-48c5-8f2f-c6c98383157f
ms.date: 12/05/2018
ms.keywords: FreeLsaHeap, FreeLsaHeap callback function [Security], LSA_FREE_LSA_HEAP, LSA_FREE_LSA_HEAP callback, _lsa_freelsaheap, ntlsa/FreeLsaHeap, security.freelsaheap
req.header: ntlsa.h
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
 - LSA_FREE_LSA_HEAP
 - ntlsa/LSA_FREE_LSA_HEAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ntlsa.h
api_name:
 - FreeLsaHeap
---

# LSA_FREE_LSA_HEAP callback function


## -description

Deallocates heap memory previously allocated by 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap">AllocateLsaHeap</a>.

## -parameters

### -param Base [in]

Pointer to the buffer to be freed.

## -returns

This function does not return a value. However, if the function sets <i>Base</i> to <b>NULL</b>, the buffer was freed. If <i>Base</i> is not <b>NULL</b> after the function call ends, the buffer could not be freed.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>