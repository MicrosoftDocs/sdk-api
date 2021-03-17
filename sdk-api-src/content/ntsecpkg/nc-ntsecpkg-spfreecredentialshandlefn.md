---
UID: NC:ntsecpkg.SpFreeCredentialsHandleFn
title: SpFreeCredentialsHandleFn (ntsecpkg.h)
description: Frees credentials acquired by calling the SpAcquireCredentialsHandle function.
helpviewer_keywords: ["SpFreeCredentialsHandle","SpFreeCredentialsHandle callback function [Security]","SpFreeCredentialsHandleFn","SpFreeCredentialsHandleFn callback","_ssp_spfreecredentialshandle","ntsecpkg/SpFreeCredentialsHandle","security.spfreecredentialshandle"]
old-location: security\spfreecredentialshandle.htm
tech.root: security
ms.assetid: c8364202-d366-47a2-bc4a-c899588a78db
ms.date: 12/05/2018
ms.keywords: SpFreeCredentialsHandle, SpFreeCredentialsHandle callback function [Security], SpFreeCredentialsHandleFn, SpFreeCredentialsHandleFn callback, _ssp_spfreecredentialshandle, ntsecpkg/SpFreeCredentialsHandle, security.spfreecredentialshandle
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
 - SpFreeCredentialsHandleFn
 - ntsecpkg/SpFreeCredentialsHandleFn
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
 - SpFreeCredentialsHandle
---

# SpFreeCredentialsHandleFn callback function


## -description

Frees <a href="/windows/desktop/SecGloss/c-gly">credentials</a> acquired by calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn">SpAcquireCredentialsHandle</a> function.

## -parameters

### -param CredentialHandle [in]

A handle to the credentials to free.

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

SSP/APs must implement the <b>SpFreeCredentialsHandle</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpFreeCredentialsHandle</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn">SpAcquireCredentialsHandle</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>