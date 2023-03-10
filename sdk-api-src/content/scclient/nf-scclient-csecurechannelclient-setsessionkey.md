---
UID: NF:scclient.CSecureChannelClient.SetSessionKey
title: CSecureChannelClient::SetSessionKey (scclient.h)
description: The SetSessionKey method sets the key for this session that is used to communicate with another component. This method is not used by applications.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","SetSessionKey method","CSecureChannelClient.SetSessionKey","CSecureChannelClient::SetSessionKey","CSecureChannelClientSetSessionKey","SetSessionKey","SetSessionKey method [windows Media Device Manager]","SetSessionKey method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::SetSessionKey","wmdm.csecurechannelclient_setsessionkey"]
old-location: wmdm\csecurechannelclient_setsessionkey.htm
tech.root: WMDM
ms.assetid: a57ffca0-3098-415c-bea5-a3ea9efbd591
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],SetSessionKey method, CSecureChannelClient.SetSessionKey, CSecureChannelClient::SetSessionKey, CSecureChannelClientSetSessionKey, SetSessionKey, SetSessionKey method [windows Media Device Manager], SetSessionKey method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::SetSessionKey, wmdm.csecurechannelclient_setsessionkey
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
 - CSecureChannelClient::SetSessionKey
 - scclient/CSecureChannelClient::SetSessionKey
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
 - CSecureChannelClient.SetSessionKey
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
<td>The pbSPSessionKey parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>



<a href="/previous-versions/bb231590(v=vs.85)">CSecureChannelClient::GetSessionKey</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>