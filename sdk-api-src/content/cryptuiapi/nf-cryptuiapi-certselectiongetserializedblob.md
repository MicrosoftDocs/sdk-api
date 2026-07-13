---
UID: NF:cryptuiapi.CertSelectionGetSerializedBlob
title: CertSelectionGetSerializedBlob function (cryptuiapi.h)
description: A helper function used to retrieve a serialized certificate BLOB from a CERT_SELECTUI_INPUT structure.
helpviewer_keywords: ["CertSelectionGetSerializedBlob","CertSelectionGetSerializedBlob function [Security]","cryptuiapi/CertSelectionGetSerializedBlob","security.certselectiongetserializedblob"]
old-location: security\certselectiongetserializedblob.htm
tech.root: security
ms.assetid: 6c3240f7-5121-401d-a4d4-df3055cb301a
ms.date: 12/05/2018
ms.keywords: CertSelectionGetSerializedBlob, CertSelectionGetSerializedBlob function [Security], cryptuiapi/CertSelectionGetSerializedBlob, security.certselectiongetserializedblob
req.header: cryptuiapi.h
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
req.lib: cryptui.lib
req.dll: Cryptui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertSelectionGetSerializedBlob
 - cryptuiapi/CertSelectionGetSerializedBlob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
 - Ext-MS-Win-security-cryptui-l1-1-0.dll
 - ext-ms-win-security-cryptui-l1-1-1.dll
 - CertCredProviderOneCore.dll
api_name:
 - CertSelectionGetSerializedBlob
---

# CertSelectionGetSerializedBlob function


## -description

The <b>CertSelectionGetSerializedBlob</b> function is a helper function used to retrieve a serialized certificate <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> from a <a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cert_selectui_input">CERT_SELECTUI_INPUT</a> structure.

## -parameters

### -param pcsi [in]

A pointer to a <a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cert_selectui_input">CERT_SELECTUI_INPUT</a> structure that contains the certificate store and certificate context chain information.

### -param ppOutBuffer [out]

The address of a pointer to a buffer that receives the serialized certificates BLOB.

### -param pulOutBufferSize [out]

A pointer to a <b>ULONG</b> to receive the size, in bytes, of the BLOB received in the buffer pointed to by the <i>ppOutBuffer</i> parameter.

## -returns

If the function succeeds, the function returns <b>S_OK</b>. 

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. 	If both <b>hStore</b> and <b>prgpChain</b> parameters are not <b>NULL</b>, return <b>E_INVALIDARG</b>. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The returned serialized BLOB is passed to the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> function in the <i>pvInAuthBuffer</i> parameter to allow a user to select a certificate by using the credential selection UI.

The certificates that are serialized in the BLOB returned in the buffer pointed to by the <i>ppOutBuffer</i>  parameter of this function are dependent on the values  of the <b>hStore</b> and <b>prgpChain</b> members of the <a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cert_selectui_input">CERT_SELECTUI_INPUT</a> structure. 

<table>
<tr>
<th><b>hStore</b></th>
<th><b>prgpChain</b></th>
<th>Certificates serialized</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
not <b>NULL</b>

</td>
<td>
The certificates pointed to by the <b>prgpChain</b> member are serialized.

</td>
</tr>
<tr>
<td>
not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
The certificates specified by the <b>hStore</b> member are serialized.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
An empty BLOB is returned.

</td>
</tr>
<tr>
<td>
not <b>NULL</b>

</td>
<td>
not <b>NULL</b>

</td>
<td>
The call fails and the function returns <b>E_INVALIDARG</b>.

</td>
</tr>
</table>