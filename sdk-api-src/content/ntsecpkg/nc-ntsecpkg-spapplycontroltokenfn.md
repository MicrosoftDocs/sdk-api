---
UID: NC:ntsecpkg.SpApplyControlTokenFn
title: SpApplyControlTokenFn (ntsecpkg.h)
description: Applies a control token to a security context. This function is not currently called by the Local Security Authority (LSA).
helpviewer_keywords: ["SpApplyControlToken","SpApplyControlToken callback function [Security]","SpApplyControlTokenFn","SpApplyControlTokenFn callback","_ssp_spapplycontroltoken","ntsecpkg/SpApplyControlToken","security.spapplycontroltoken"]
old-location: security\spapplycontroltoken.htm
tech.root: security
ms.assetid: 60c5e310-dd80-4bf7-9480-ac614c98d75f
ms.date: 12/05/2018
ms.keywords: SpApplyControlToken, SpApplyControlToken callback function [Security], SpApplyControlTokenFn, SpApplyControlTokenFn callback, _ssp_spapplycontroltoken, ntsecpkg/SpApplyControlToken, security.spapplycontroltoken
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
 - SpApplyControlTokenFn
 - ntsecpkg/SpApplyControlTokenFn
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
 - SpApplyControlToken
---

# SpApplyControlTokenFn callback function


## -description

Applies a control token to a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. This function is not currently called by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA).

## -parameters

### -param ContextHandle [in]

A handle to the security context to be modified based on the <i>ControlToken</i> parameter.

### -param ControlToken [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure containing the token to apply to the context.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists common reasons for failure and the error codes that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The token is not valid.

</td>
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

SSP/APs must implement the <b>SpApplyControlToken</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpApplyControlToken</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>