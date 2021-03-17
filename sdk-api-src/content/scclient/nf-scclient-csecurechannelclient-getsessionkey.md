---
UID: NF:scclient.CSecureChannelClient.GetSessionKey
title: CSecureChannelClient::GetSessionKey (scclient.h)
description: The GetSessionKey method retrieves the current session key. This method is not used by applications.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","GetSessionKey method","CSecureChannelClient.GetSessionKey","CSecureChannelClient::GetSessionKey","CSecureChannelClientGetSessionKey","GetSessionKey","GetSessionKey method [windows Media Device Manager]","GetSessionKey method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::GetSessionKey","wmdm.csecurechannelclient_getsessionkey"]
old-location: wmdm\csecurechannelclient_getsessionkey.htm
tech.root: WMDM
ms.assetid: b5963027-ef6e-44e0-a1ed-31ac82477002
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],GetSessionKey method, CSecureChannelClient.GetSessionKey, CSecureChannelClient::GetSessionKey, CSecureChannelClientGetSessionKey, GetSessionKey, GetSessionKey method [windows Media Device Manager], GetSessionKey method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::GetSessionKey, wmdm.csecurechannelclient_getsessionkey
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
 - CSecureChannelClient::GetSessionKey
 - scclient/CSecureChannelClient::GetSessionKey
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
 - CSecureChannelClient.GetSessionKey
---

# CSecureChannelClient::GetSessionKey


## -description

The <b>GetSessionKey</b> method retrieves the current session key. This method is not used by applications.

## -parameters

### -param pbSPSessionKey [out]

Pointer to the first byte of a buffer specifying the session key. The session key is used for encryption and decryption by the <a href="/previous-versions/bb231587(v=vs.85)">EncryptParam</a> and <a href="/previous-versions/bb231586(v=vs.85)">DecryptParam</a> methods.

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



<a href="/previous-versions/ms868506(v=msdn.10)">CSecureChannelClient::SetSessionKey</a>