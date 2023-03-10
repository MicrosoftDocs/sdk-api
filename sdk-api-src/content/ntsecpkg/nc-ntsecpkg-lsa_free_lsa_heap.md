---
UID: NC:ntsecpkg.LSA_FREE_LSA_HEAP
title: LSA_FREE_LSA_HEAP (ntsecpkg.h)
description: The FreeReturnBuffer function is used to free buffers allocated by the Local Security Authority (LSA) and returned to the security package. The package calls this function when the information in the returned buffer is no longer needed.
helpviewer_keywords: ["FreeReturnBuffer","FreeReturnBuffer callback function [Security]","LSA_FREE_LSA_HEAP","LSA_FREE_LSA_HEAP callback","_ssp_freereturnbuffer","ntsecpkg/FreeReturnBuffer","security.freereturnbuffer"]
old-location: security\freereturnbuffer.htm
tech.root: security
ms.assetid: 44b7e6f2-eb7e-47ec-8252-689eb1e5aa77
ms.date: 12/05/2018
ms.keywords: FreeReturnBuffer, FreeReturnBuffer callback function [Security], LSA_FREE_LSA_HEAP, LSA_FREE_LSA_HEAP callback, _ssp_freereturnbuffer, ntsecpkg/FreeReturnBuffer, security.freereturnbuffer
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
 - LSA_FREE_LSA_HEAP
 - ntsecpkg/LSA_FREE_LSA_HEAP
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
 - FreeReturnBuffer
---

# LSA_FREE_LSA_HEAP callback function


## -description

The <b>FreeReturnBuffer</b> function is used to free buffers allocated by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) and returned to the <a href="/windows/desktop/SecGloss/s-gly">security package</a>. The package calls this function when the information in the returned buffer is no longer needed.

## -parameters

### -param Base [in]

Pointer to the buffer to free.

## -remarks

A pointer to the <b>FreeReturnBuffer</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>