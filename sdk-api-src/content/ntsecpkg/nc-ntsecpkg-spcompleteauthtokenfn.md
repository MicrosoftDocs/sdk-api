---
UID: NC:ntsecpkg.SpCompleteAuthTokenFn
title: SpCompleteAuthTokenFn (ntsecpkg.h)
description: Completes an authentication token.S
helpviewer_keywords: ["SpCompleteAuthToken","SpCompleteAuthToken callback function [Security]","SpCompleteAuthTokenFn","SpCompleteAuthTokenFn callback","_ssp_spcompleteauthtoken","ntsecpkg/SpCompleteAuthToken","security.spcompleteauthtoken"]
old-location: security\spcompleteauthtoken.htm
tech.root: security
ms.assetid: 2e20620a-457d-424c-a6b9-64b571174c98
ms.date: 12/05/2018
ms.keywords: SpCompleteAuthToken, SpCompleteAuthToken callback function [Security], SpCompleteAuthTokenFn, SpCompleteAuthTokenFn callback, _ssp_spcompleteauthtoken, ntsecpkg/SpCompleteAuthToken, security.spcompleteauthtoken
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
 - SpCompleteAuthTokenFn
 - ntsecpkg/SpCompleteAuthTokenFn
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
 - SpCompleteAuthToken
---

# SpCompleteAuthTokenFn callback function


## -description

The <b>SpCompleteAuthToken</b> function completes an authentication token.

The <b>SpCompleteAuthToken</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-completeauthtoken">CompleteAuthToken</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param ContextHandle [in]

Handle of the context to complete.

### -param InputBuffer [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains package-specific information for the context.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>

## -remarks

SSP/APs must implement the <b>SpCompleteAuthToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpCompleteAuthToken</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-completeauthtoken">CompleteAuthToken</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>
