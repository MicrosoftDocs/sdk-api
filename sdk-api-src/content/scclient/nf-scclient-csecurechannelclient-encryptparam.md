---
UID: NF:scclient.CSecureChannelClient.EncryptParam
title: CSecureChannelClient::EncryptParam
author: windows-sdk-content
description: The EncryptParam method encrypts data being sent out through a parameter. Data is encrypted in-place, in the submitted buffer.
old-location: wmdm\csecurechannelclient_encryptparam.htm
old-project: WMDM
ms.assetid: 7c71c2d4-b337-487f-a04a-87536f84f03e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],EncryptParam method, CSecureChannelClient.EncryptParam, CSecureChannelClient::EncryptParam, CSecureChannelClientEncryptParam, EncryptParam, EncryptParam method [windows Media Device Manager], EncryptParam method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::EncryptParam, wmdm.csecurechannelclient_encryptparam
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scclient.h
req.include-header: 
req.redist: 
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
 - CSecureChannelClient.EncryptParam
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.

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



This method is used to encrypt data before sending it to the device in <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.

Encrypt only the parameters that are specified as requiring encryption. See <a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a> for a table of methods that must use the message authentication code algorithm and encrypted parameters.

For example code, see <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.




## -see-also




<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>



<a href="https://msdn.microsoft.com/4e19b86c-9efc-4c20-bac9-8cd6b944f69e">CSecureChannelClient::DecryptParam</a>



<a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

