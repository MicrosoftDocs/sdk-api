---
UID: NC:ntsecpkg.SpUpdateCredentialsFn
title: SpUpdateCredentialsFn (ntsecpkg.h)
description: Updates the credentials associated with the specified context.
helpviewer_keywords: ["SEC_WINNT_AUTH_DATA_TYPE_CERT","SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA","SEC_WINNT_AUTH_DATA_TYPE_PASSWORD","SpUpdateCredentialsFn","SpUpdateCredentialsFn callback","SpUpdateCredentialsFn callback function [Security]","ntsecpkg/SpUpdateCredentialsFn","security.spupdatecredentialsfn"]
old-location: security\spupdatecredentialsfn.htm
tech.root: security
ms.assetid: 56aba12e-a335-4d16-81b0-7ab521f872e7
ms.date: 12/05/2018
ms.keywords: SEC_WINNT_AUTH_DATA_TYPE_CERT, SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA, SEC_WINNT_AUTH_DATA_TYPE_PASSWORD, SpUpdateCredentialsFn, SpUpdateCredentialsFn callback, SpUpdateCredentialsFn callback function [Security], ntsecpkg/SpUpdateCredentialsFn, security.spupdatecredentialsfn
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - SpUpdateCredentialsFn
 - ntsecpkg/SpUpdateCredentialsFn
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
 - SpUpdateCredentialsFn
---

# SpUpdateCredentialsFn callback function


## -description

Updates the credentials associated with the specified context.

## -parameters

### -param ContextHandle [in]

A handle to the context to update.

### -param *CredType [in]

The type of credential specified by the <i>ContextHandle</i> parameter. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_DATA_TYPE_PASSWORD"></a><a id="sec_winnt_auth_data_type_password"></a><dl>
<dt><b>SEC_WINNT_AUTH_DATA_TYPE_PASSWORD</b></dt>
<dt>0x28bfc32f, 0x10f6, 0x4738,  0x98, 0xd1, 0x1a, 0xc0, 0x61, 0xdf, 0x71, 0x6a</dt>
</dl>
</td>
<td width="60%">
The credential is a password.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_DATA_TYPE_CERT"></a><a id="sec_winnt_auth_data_type_cert"></a><dl>
<dt><b>SEC_WINNT_AUTH_DATA_TYPE_CERT</b></dt>
<dt>0x235f69ad, 0x73fb, 0x4dbc,  0x82, 0x3, 0x6, 0x29, 0xe7, 0x39, 0x33, 0x9b</dt>
</dl>
</td>
<td width="60%">
The credential is a certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA"></a><a id="sec_winnt_auth_data_type_csp_data"></a><dl>
<dt><b>SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA</b></dt>
<dt>0x68fd9879, 0x79c, 0x4dfe,  0x82, 0x81, 0x57, 0x8a, 0xad, 0xc1, 0xc1, 0x0</dt>
</dl>
</td>
<td width="60%">
The credential is authentication data from a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

</td>
</tr>
</table>

### -param FlatCredUIContextLength [in]

The size, in characters, of the buffer specified by  the <i>FlatCredUIContext</i> parameter.

### -param FlatCredUIContext

A string that specifies the updated credentials.

## -returns

If the function succeeds, return <b>STATUS_SUCCESS</b>, or an informational status code.

If the function fails, return an <b>NTSTATUS</b> error code that indicates the reason it failed. For more information, see Remarks.

## -remarks

A pointer to the <b>SpUpdateCredentialsFn</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.