---
UID: NF:mbnapi.IMbnConnection.Disconnect
title: IMbnConnection::Disconnect (mbnapi.h)
description: Disconnects a data connection.
helpviewer_keywords: ["Disconnect","Disconnect method [Microsoft Broadband Networks]","Disconnect method [Microsoft Broadband Networks]","IMbnConnection interface","IMbnConnection interface [Microsoft Broadband Networks]","Disconnect method","IMbnConnection.Disconnect","IMbnConnection::Disconnect","mbn.imbnconnection_disconnect","mbnapi/IMbnConnection::Disconnect"]
old-location: mbn\imbnconnection_disconnect.htm
tech.root: mbn
ms.assetid: bc7f28db-499d-41be-a2cc-b4940a5bccd6
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [Microsoft Broadband Networks], Disconnect method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],Disconnect method, IMbnConnection.Disconnect, IMbnConnection::Disconnect, mbn.imbnconnection_disconnect, mbnapi/IMbnConnection::Disconnect
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnConnection::Disconnect
 - mbnapi/IMbnConnection::Disconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnection.Disconnect
---

# IMbnConnection::Disconnect


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Disconnects a data connection.

## -parameters

### -param requestID [out]

A pointer to a unique request ID assigned by the Mobile Broadband service to identify this asynchronous request.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The connection has already been disconnected.

</td>
</tr>
</table>

## -remarks

Deactivation will also result in the disconnection of the L2 connection.

This is an asynchronous operation that will return immediately. If this method returns successfully, then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionevents-ondisconnectcomplete">OnDisconnectComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a> when the operation is complete.

Windows 8 and later versions of Windows: A Windows Store app may only use <b>Disconnect</b> if the existing MBN connection was initiated by that app using <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">Connect</a>. <b>Disconnect</b> may not be used to disconnect connections that have been made by the user or by the <a href="/windows/desktop/wcm/windows-connection-manager-portal">Windows Connection Manager</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a>