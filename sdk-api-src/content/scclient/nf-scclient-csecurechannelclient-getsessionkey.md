---
UID: NF:scclient.CSecureChannelClient.GetSessionKey
title: CSecureChannelClient::GetSessionKey
author: windows-sdk-content
description: The GetSessionKey method retrieves the current session key. This method is not used by applications.
old-location: wmdm\csecurechannelclient_getsessionkey.htm
tech.root: WMDM
ms.assetid: b5963027-ef6e-44e0-a1ed-31ac82477002
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],GetSessionKey method, CSecureChannelClient.GetSessionKey, CSecureChannelClient::GetSessionKey, CSecureChannelClientGetSessionKey, GetSessionKey, GetSessionKey method [windows Media Device Manager], GetSessionKey method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::GetSessionKey, wmdm.csecurechannelclient_getsessionkey
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelClient.GetSessionKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CSecureChannelClient::GetSessionKey


## -description



The <b>GetSessionKey</b> method retrieves the current session key. This method is not used by applications.




## -parameters




### -param pbSPSessionKey [out]

Pointer to the first byte of a buffer specifying the session key. The session key is used for encryption and decryption by the <a href="https://msdn.microsoft.com/7c71c2d4-b337-487f-a04a-87536f84f03e">EncryptParam</a> and <a href="https://msdn.microsoft.com/4e19b86c-9efc-4c20-bac9-8cd6b944f69e">DecryptParam</a> methods.


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
<td>The pbSPSessionKey parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>



<a href="https://msdn.microsoft.com/a57ffca0-3098-415c-bea5-a3ea9efbd591">CSecureChannelClient::SetSessionKey</a>
 

 

