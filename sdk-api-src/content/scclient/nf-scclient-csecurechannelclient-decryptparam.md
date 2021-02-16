---
UID: NF:scclient.CSecureChannelClient.DecryptParam
title: CSecureChannelClient::DecryptParam (scclient.h)
description: The DecryptParam method decrypts data received through a parameter. Encryption is performed in-place on the encrypted data.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","DecryptParam method","CSecureChannelClient.DecryptParam","CSecureChannelClient::DecryptParam","CSecureChannelClientDecryptParam","DecryptParam","DecryptParam method [windows Media Device Manager]","DecryptParam method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::DecryptParam","wmdm.csecurechannelclient_decryptparam"]
old-location: wmdm\csecurechannelclient_decryptparam.htm
tech.root: WMDM
ms.assetid: 4e19b86c-9efc-4c20-bac9-8cd6b944f69e
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],DecryptParam method, CSecureChannelClient.DecryptParam, CSecureChannelClient::DecryptParam, CSecureChannelClientDecryptParam, DecryptParam, DecryptParam method [windows Media Device Manager], DecryptParam method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::DecryptParam, wmdm.csecurechannelclient_decryptparam
req.header: scclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CSecureChannelClient::DecryptParam
 - scclient/CSecureChannelClient::DecryptParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelClient.DecryptParam
---

# CSecureChannelClient::DecryptParam


## -description

The <b>DecryptParam</b> method decrypts data received through a parameter. Encryption is performed in-place on the encrypted data.

## -parameters

### -param pbData [in, out]

Pointer to the data buffer that holds the information to decrypt. On input contains the encrypted data; on output, contains the decrypted data. The decrypted data is the same length as the encrypted data.

### -param dwDataLen [in]

Pointer to a <b>DWORD</b> specifying the length of the buffer to which <i>pbData</i> points.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

This is used by <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a> to decrypt data read from the device.

For robustness, before calling the <b>DecryptParam</b> method, components should copy the data to a temporary buffer and then use <b>DecryptParam</b> to decrypt the temporary buffer. Decryption is handled in-place in the buffer; the buffer does not need to be resized.

For example code, see <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>



<a href="/previous-versions/bb231587(v=vs.85)">CSecureChannelClient::EncryptParam</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>