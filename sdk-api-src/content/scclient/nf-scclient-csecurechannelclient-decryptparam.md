---
UID: NF:scclient.CSecureChannelClient.DecryptParam
title: CSecureChannelClient::DecryptParam
author: windows-sdk-content
description: The DecryptParam method decrypts data received through a parameter. Encryption is performed in-place on the encrypted data.
old-location: wmdm\csecurechannelclient_decryptparam.htm
old-project: WMDM
ms.assetid: 4e19b86c-9efc-4c20-bac9-8cd6b944f69e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],DecryptParam method, CSecureChannelClient.DecryptParam, CSecureChannelClient::DecryptParam, CSecureChannelClientDecryptParam, DecryptParam, DecryptParam method [windows Media Device Manager], DecryptParam method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::DecryptParam, wmdm.csecurechannelclient_decryptparam
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_SB_SORT_BY
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

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



This is used by <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a> to decrypt data read from the device.

For robustness, before calling the <b>DecryptParam</b> method, components should copy the data to a temporary buffer and then use <b>DecryptParam</b> to decrypt the temporary buffer. Decryption is handled in-place in the buffer; the buffer does not need to be resized.

For example code, see <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.




## -see-also




<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>



<a href="https://msdn.microsoft.com/7c71c2d4-b337-487f-a04a-87536f84f03e">CSecureChannelClient::EncryptParam</a>



<a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

