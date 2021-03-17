---
UID: NF:scserver.CSecureChannelServer.MACFinal
title: CSecureChannelServer::MACFinal (scserver.h)
description: The MACFinal method releases the message authentication code (MAC) channel and retrieves a final MAC value.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","MACFinal method","CSecureChannelServer.MACFinal","CSecureChannelServer::MACFinal","CSecureChannelServerMACFinal","MACFinal","MACFinal method [windows Media Device Manager]","MACFinal method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::MACFinal","wmdm.csecurechannelserver_macfinal"]
old-location: wmdm\csecurechannelserver_macfinal.htm
tech.root: WMDM
ms.assetid: 047340a5-5382-443e-a6d5-ecbcdfe9a210
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],MACFinal method, CSecureChannelServer.MACFinal, CSecureChannelServer::MACFinal, CSecureChannelServerMACFinal, MACFinal, MACFinal method [windows Media Device Manager], MACFinal method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::MACFinal, wmdm.csecurechannelserver_macfinal
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
 - CSecureChannelServer::MACFinal
 - scserver/CSecureChannelServer::MACFinal
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
 - CSecureChannelServer.MACFinal
---

# CSecureChannelServer::MACFinal


## -description

The <b>MACFinal</b> method releases the message authentication code (MAC) channel and retrieves a final MAC value.

## -parameters

### -param hMAC [in]

Handle to the MAC for the current parameter data. The handle is returned from the <b>MACInit</b> method. The handle is no longer valid after this method call.

### -param abData [out]

Pointer to an 8-byte buffer to receive the final MAC value for the current parameter data.

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
<td>A parameter is invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/ms868514(v=msdn.10)">CSecureChannelServer::MACInit</a>



<a href="/previous-versions/ms868515(v=msdn.10)">CSecureChannelServer::MACUpdate</a>



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>