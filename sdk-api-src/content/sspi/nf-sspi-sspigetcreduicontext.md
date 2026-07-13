---
UID: NF:sspi.SspiGetCredUIContext
title: SspiGetCredUIContext function (sspi.h)
description: Retrieves context information from a credential provider. (SspiGetCredUIContext)
helpviewer_keywords: ["SEC_WINNT_AUTH_DATA_TYPE_CERT","SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA","SEC_WINNT_AUTH_DATA_TYPE_PASSWORD","SspiGetCredUIContext","SspiGetCredUIContext function [Security]","security.sspigetcreduicontext","sspi/SspiGetCredUIContext"]
old-location: security\sspigetcreduicontext.htm
tech.root: security
ms.assetid: 9da39bc4-ece8-493f-b9fd-5f8ba9ed288e
ms.date: 12/05/2018
ms.keywords: SEC_WINNT_AUTH_DATA_TYPE_CERT, SEC_WINNT_AUTH_DATA_TYPE_CSP_DATA, SEC_WINNT_AUTH_DATA_TYPE_PASSWORD, SspiGetCredUIContext, SspiGetCredUIContext function [Security], security.sspigetcreduicontext, sspi/SspiGetCredUIContext
req.header: sspi.h
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
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiGetCredUIContext
 - sspi/SspiGetCredUIContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - SspiGetCredUIContext
---

# SspiGetCredUIContext function


## -description

Retrieves context information from a credential provider.

## -parameters

### -param ContextHandle [in]

A pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_credui_context">SEC_WINNT_CREDUI_CONTEXT</a> structure retrieved during a previous call to the <a href="/windows/desktop/api/sspi/nf-sspi-sspiunmarshalcreduicontext">SspiUnmarshalCredUIContext</a> function.

### -param CredType [in]

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

### -param LogonId [in]

The logon ID associated with the credential specified by the <i>ContextHandle</i> parameter.

The caller must be running as <b>LocalSystem</b> to specify a logon ID.

### -param CredUIContexts [out]

A pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_credui_context_vector">SEC_WINNT_CREDUI_CONTEXT_VECTOR</a> structure that specifies the offset and size of the data in the structure specified by the <i>ContextHandle</i> parameter.

### -param TokenHandle [out]

A handle to the specified user's token.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.
