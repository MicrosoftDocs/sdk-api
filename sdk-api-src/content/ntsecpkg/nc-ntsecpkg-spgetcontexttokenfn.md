---
UID: NC:ntsecpkg.SpGetContextTokenFn
title: SpGetContextTokenFn (ntsecpkg.h)
description: Obtains the token to impersonate.
helpviewer_keywords: ["SpGetContextToken","SpGetContextToken callback function [Security]","SpGetContextTokenFn","SpGetContextTokenFn callback","_ssp_spgetcontexttoken","ntsecpkg/SpGetContextToken","security.spgetcontexttoken"]
old-location: security\spgetcontexttoken.htm
tech.root: security
ms.assetid: d2e6b57d-751d-4f07-b05b-6d3aabd60650
ms.date: 12/05/2018
ms.keywords: SpGetContextToken, SpGetContextToken callback function [Security], SpGetContextTokenFn, SpGetContextTokenFn callback, _ssp_spgetcontexttoken, ntsecpkg/SpGetContextToken, security.spgetcontexttoken
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
 - SpGetContextTokenFn
 - ntsecpkg/SpGetContextTokenFn
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
 - SpGetContextToken
---

# SpGetContextTokenFn callback function


## -description

Obtains the token to impersonate. The <b>SpGetContextToken</b> function is used by the SSPI 
<a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a> function to obtain the token to impersonate.

## -parameters

### -param ContextHandle [in]

A handle to the context to impersonate.

### -param ImpersonationToken [out]

Pointer that receives a handle to the token for the specified context. Return the handle to the token without first duplicating the handle or the token.

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

SSP/APs must implement the <b>SpGetContextToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetContextToken</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_user_function_table">SECPKG_USER_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spusermodeinitializefn">SpUserModeInitialize</a>