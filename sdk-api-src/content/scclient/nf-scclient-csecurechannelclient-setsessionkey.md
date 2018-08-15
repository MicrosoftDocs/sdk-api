---
UID: NF:scclient.CSecureChannelClient.SetSessionKey
title: CSecureChannelClient::SetSessionKey
author: windows-sdk-content
description: The SetSessionKey method sets the key for this session that is used to communicate with another component. This method is not used by applications.
old-location: wmdm\csecurechannelclient_setsessionkey.htm
old-project: WMDM
ms.assetid: a57ffca0-3098-415c-bea5-a3ea9efbd591
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],SetSessionKey method, CSecureChannelClient.SetSessionKey, CSecureChannelClient::SetSessionKey, CSecureChannelClientSetSessionKey, SetSessionKey, SetSessionKey method [windows Media Device Manager], SetSessionKey method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::SetSessionKey, wmdm.csecurechannelclient_setsessionkey
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
 - CSecureChannelClient.SetSessionKey
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelClient::SetSessionKey


## -description



The <b>SetSessionKey</b> method sets the key for this session that is used to communicate with another component. This method is not used by applications.




## -parameters




### -param pbSPSessionKey [in]

Pointer to the first byte of the session key that is to be set.


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



<a href="https://msdn.microsoft.com/b5963027-ef6e-44e0-a1ed-31ac82477002">CSecureChannelClient::GetSessionKey</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

