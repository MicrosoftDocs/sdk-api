---
UID: NF:scserver.CSecureChannelServer.MACUpdate
title: CSecureChannelServer::MACUpdate (scserver.h)
description: The MACUpdate method updates the message authentication code (MAC) value with a parameter value.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","MACUpdate method","CSecureChannelServer.MACUpdate","CSecureChannelServer::MACUpdate","CSecureChannelServerMACUpdate","MACUpdate","MACUpdate method [windows Media Device Manager]","MACUpdate method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::MACUpdate","wmdm.csecurechannelserver_macupdate"]
old-location: wmdm\csecurechannelserver_macupdate.htm
tech.root: WMDM
ms.assetid: f8b5548d-ffd5-4dc3-8d08-61a65841a997
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],MACUpdate method, CSecureChannelServer.MACUpdate, CSecureChannelServer::MACUpdate, CSecureChannelServerMACUpdate, MACUpdate, MACUpdate method [windows Media Device Manager], MACUpdate method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::MACUpdate, wmdm.csecurechannelserver_macupdate
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
 - CSecureChannelServer::MACUpdate
 - scserver/CSecureChannelServer::MACUpdate
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
 - CSecureChannelServer.MACUpdate
---

# CSecureChannelServer::MACUpdate


## -description

The <b>MACUpdate</b> method updates the message authentication code (MAC) value with a parameter value.

## -parameters

### -param hMAC [in]

Handle to the array containing the MAC for the current parameter data. The handle is returned by the <b>MACInit</b> method.

### -param pbData [in]

Pointer to the data to be added to the MAC value for the current parameter data.

### -param dwDataLen

<b>DWORD</b> specifying the length of the data to which <i>pbData</i> points.

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

<b>MACUpdate</b> must be called repeatedly with each piece of data to add to the message authentication code (MAC) . <b>MACUpdate</b> must be called after <b>MACInit</b> because <b>MACInit</b> acquires the MAC handle. <b>MACFinal</b> must be called after <b>MACUpdate</b>.


#### Examples

See the example code for <a href="/previous-versions/ms868514(v=msdn.10)">MACInit</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/ms868514(v=msdn.10)">CSecureChannelServer::MACInit</a>



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>