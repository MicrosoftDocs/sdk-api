---
UID: NF:scserver.CSecureChannelServer.GetAppSec
title: CSecureChannelServer::GetAppSec (scserver.h)
description: The GetAppSec method retrieves the application security levels of the local and remote components. This method is published and available, but normally is used only by Windows Media Device Manager.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","GetAppSec method","CSecureChannelServer.GetAppSec","CSecureChannelServer::GetAppSec","CSecureChannelServerGetAppSec","GetAppSec","GetAppSec method [windows Media Device Manager]","GetAppSec method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::GetAppSec","wmdm.csecurechannelserver_getappsec"]
old-location: wmdm\csecurechannelserver_getappsec.htm
tech.root: WMDM
ms.assetid: 60659c36-ef9a-46fd-9a61-4a5a5210fd1f
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],GetAppSec method, CSecureChannelServer.GetAppSec, CSecureChannelServer::GetAppSec, CSecureChannelServerGetAppSec, GetAppSec, GetAppSec method [windows Media Device Manager], GetAppSec method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::GetAppSec, wmdm.csecurechannelserver_getappsec
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
 - CSecureChannelServer::GetAppSec
 - scserver/CSecureChannelServer::GetAppSec
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
 - CSecureChannelServer.GetAppSec
---

# CSecureChannelServer::GetAppSec


## -description

The <b>GetAppSec</b> method retrieves the application security levels of the local and remote components. This method is published and available, but normally is used only by Windows Media Device Manager.

## -parameters

### -param pdwLocalAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the local component.

### -param pdwRemoteAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the remote component.

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

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>