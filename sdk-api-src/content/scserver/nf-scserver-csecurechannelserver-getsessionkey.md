---
UID: NF:scserver.CSecureChannelServer.GetSessionKey
title: CSecureChannelServer::GetSessionKey (scserver.h)
description: The GetSessionKey method retrieves the current session key that is used for encryption and decryption. This method is published and available, but normally is used only by Windows Media Device Manager.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","GetSessionKey method","CSecureChannelServer.GetSessionKey","CSecureChannelServer::GetSessionKey","CSecureChannelServerGetSessionKey","GetSessionKey","GetSessionKey method [windows Media Device Manager]","GetSessionKey method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::GetSessionKey","wmdm.csecurechannelserver_getsessionkey"]
old-location: wmdm\csecurechannelserver_getsessionkey.htm
tech.root: WMDM
ms.assetid: 1be09669-434e-4774-92bf-4ea470d6c4b9
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],GetSessionKey method, CSecureChannelServer.GetSessionKey, CSecureChannelServer::GetSessionKey, CSecureChannelServerGetSessionKey, GetSessionKey, GetSessionKey method [windows Media Device Manager], GetSessionKey method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::GetSessionKey, wmdm.csecurechannelserver_getsessionkey
req.header: scserver.h
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
 - CSecureChannelServer::GetSessionKey
 - scserver/CSecureChannelServer::GetSessionKey
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
 - CSecureChannelServer.GetSessionKey
---

# CSecureChannelServer::GetSessionKey


## -description

The <b>GetSessionKey</b> method retrieves the current session key that is used for encryption and decryption. This method is published and available, but normally is used only by Windows Media Device Manager.

## -parameters

### -param pbSPSessionKey [out]

Pointer to the first byte of a buffer containing the session key.

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

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/ms868519(v=msdn.10)">CSecureChannelServer::SetSessionKey</a>