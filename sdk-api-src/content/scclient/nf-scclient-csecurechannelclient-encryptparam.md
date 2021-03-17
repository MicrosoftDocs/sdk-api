---
UID: NF:scclient.CSecureChannelClient.EncryptParam
title: CSecureChannelClient::EncryptParam (scclient.h)
description: The EncryptParam method encrypts data being sent out through a parameter. Data is encrypted in-place, in the submitted buffer.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","EncryptParam method","CSecureChannelClient.EncryptParam","CSecureChannelClient::EncryptParam","CSecureChannelClientEncryptParam","EncryptParam","EncryptParam method [windows Media Device Manager]","EncryptParam method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::EncryptParam","wmdm.csecurechannelclient_encryptparam"]
old-location: wmdm\csecurechannelclient_encryptparam.htm
tech.root: WMDM
ms.assetid: 7c71c2d4-b337-487f-a04a-87536f84f03e
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],EncryptParam method, CSecureChannelClient.EncryptParam, CSecureChannelClient::EncryptParam, CSecureChannelClientEncryptParam, EncryptParam, EncryptParam method [windows Media Device Manager], EncryptParam method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::EncryptParam, wmdm.csecurechannelclient_encryptparam
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
 - CSecureChannelClient::EncryptParam
 - scclient/CSecureChannelClient::EncryptParam
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
 - CSecureChannelClient.EncryptParam
---

# CSecureChannelClient::EncryptParam


## -description

The <b>EncryptParam</b> method encrypts data being sent out through a parameter. Data is encrypted in-place, in the submitted buffer.

## -parameters

### -param pbData [in, out]

Pointer to the data buffer that holds the information to encrypt. Encryption is handled in-place in the buffer, and the retrieved encrypted data is the same size as the original data.

### -param dwDataLen [in]

Pointer to a <b>DWORD</b> specifying the length of the <i>pbData</i> buffer.

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

This method is used to encrypt data before sending it to the device in <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.

Encrypt only the parameters that are specified as requiring encryption. See <a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a> for a table of methods that must use the message authentication code algorithm and encrypted parameters.

For example code, see <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>



<a href="/previous-versions/bb231586(v=vs.85)">CSecureChannelClient::DecryptParam</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>