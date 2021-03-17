---
UID: NF:scserver.CSecureChannelServer.SACGetProtocols
title: CSecureChannelServer::SACGetProtocols (scserver.h)
description: The SACGetProtocols method reports the protocols supported by a component.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","SACGetProtocols method","CSecureChannelServer.SACGetProtocols","CSecureChannelServer::SACGetProtocols","CSecureChannelServerSACGetProtocols","SACGetProtocols","SACGetProtocols method [windows Media Device Manager]","SACGetProtocols method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::SACGetProtocols","wmdm.csecurechannelserver_sacgetprotocols"]
old-location: wmdm\csecurechannelserver_sacgetprotocols.htm
tech.root: WMDM
ms.assetid: 42878774-9c8b-4d80-a17e-6682da4d34ab
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],SACGetProtocols method, CSecureChannelServer.SACGetProtocols, CSecureChannelServer::SACGetProtocols, CSecureChannelServerSACGetProtocols, SACGetProtocols, SACGetProtocols method [windows Media Device Manager], SACGetProtocols method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::SACGetProtocols, wmdm.csecurechannelserver_sacgetprotocols
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
 - CSecureChannelServer::SACGetProtocols
 - scserver/CSecureChannelServer::SACGetProtocols
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
 - CSecureChannelServer.SACGetProtocols
---

# CSecureChannelServer::SACGetProtocols


## -description

The <b>SACGetProtocols</b> method reports the protocols supported by a component.

## -parameters

### -param ppdwProtocols

Pointer to a pointer to an array of <b>DWORD</b> values specifying the supported protocols.

### -param pdwProtocolCount

Pointer to a <b>DWORD</b> specifying the number of protocols in the array to which <i>ppdwProtocols</i> points.

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

This method is used by the service provider to implement the public <a href="/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols">IComponentAuthenticate::SACGetProtocols</a> method. For an example of calling this method, see that method's documentation.

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols">IComponentAuthenticate::SACGetProtocols</a>