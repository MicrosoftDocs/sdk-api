---
UID: NC:ntsecpkg.LSA_GET_CALL_INFO
title: LSA_GET_CALL_INFO (ntsecpkg.h)
description: The GetCallInfo function retrieves information about the most recent function call.
helpviewer_keywords: ["GetCallInfo","GetCallInfo callback function [Security]","LSA_GET_CALL_INFO","LSA_GET_CALL_INFO callback","_ssp_getcallinfo","ntsecpkg/GetCallInfo","security.getcallinfo"]
old-location: security\getcallinfo.htm
tech.root: security
ms.assetid: 3e59ee6a-f7ba-4886-98f7-74ffbfaadea7
ms.date: 12/05/2018
ms.keywords: GetCallInfo, GetCallInfo callback function [Security], LSA_GET_CALL_INFO, LSA_GET_CALL_INFO callback, _ssp_getcallinfo, ntsecpkg/GetCallInfo, security.getcallinfo
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
 - LSA_GET_CALL_INFO
 - ntsecpkg/LSA_GET_CALL_INFO
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
 - GetCallInfo
---

# LSA_GET_CALL_INFO callback function


## -description

The <b>GetCallInfo</b> function retrieves information about the most recent function call.

## -parameters

### -param Info [out]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_call_info">SECPKG_CALL_INFO</a> structure that receives information about the call.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

A pointer to the <b>GetCallInfo</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>