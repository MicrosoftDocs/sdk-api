---
UID: NF:mbnapi.IMbnConnection.Connect
title: IMbnConnection::Connect (mbnapi.h)
description: Establishes a data connection.
helpviewer_keywords: ["Connect","Connect method [Microsoft Broadband Networks]","Connect method [Microsoft Broadband Networks]","IMbnConnection interface","IMbnConnection interface [Microsoft Broadband Networks]","Connect method","IMbnConnection.Connect","IMbnConnection::Connect","mbn.imbnconnection_connect","mbnapi/IMbnConnection::Connect"]
old-location: mbn\imbnconnection_connect.htm
tech.root: mbn
ms.assetid: 66acb84e-8e0f-4ff1-abc4-b32f782ce9f3
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Microsoft Broadband Networks], Connect method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],Connect method, IMbnConnection.Connect, IMbnConnection::Connect, mbn.imbnconnection_connect, mbnapi/IMbnConnection::Connect
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
 - IMbnConnection::Connect
 - mbnapi/IMbnConnection::Connect
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
 - IMbnConnection.Connect
---

# IMbnConnection::Connect


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Establishes a data connection.

## -parameters

### -param connectionMode [in]

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_connection_mode">MBN_CONNECTION_MODE</a> value that specifies the mode of the connection.

### -param strProfile [in]

Contains the profile designator.

### -param requestID [out]

A pointer to a unique request ID returned by the Mobile Broadband service to identify this asynchronous request.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid profile name was specified or the <i>strProfile</i> argument is not compliant to XML profile schema

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_MAX_ACTIVATED_CONTEXTS</b></dt>
</dl>
</td>
<td width="60%">
There is already an active Mobile Broadband context.  Multiple active contexts are not supported.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">Connect</a> method is used to activate a connection context for the device. The Mobile Broadband service currently supports at most one active context. Activation of the context will also result in L2 connection also being established. Similarly, deactivation of a context will result in disconnection of the physical data connection to the mobile network.

If the device is not in the packet-attached state at the time of calling this operation then the Mobile Broadband service will implicitly packet attach the device before issuing the connect request to the device. If there is any packet service state change then application will be notified by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a> interface.

If <i>connectionMode</i> is set to <b>MBN_CONNECTION_MODE_PROFILE</b>, then <i>strProfile</i> represents the name of the profile for the device. If set to <b>MBN_CONNECTION_MODE_TMP_PROFILE</b>, then <i>strProfile</i> represents the XML representation of the profile. A calling application can use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> to get a list of connection profiles stored in the device.


This is an asynchronous operation that will return immediately. If this method returns successfully, then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionevents-onconnectcomplete">OnConnectComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a> when the operation is complete.


Windows 8 and later versions of Windows: A Windows Store app may use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">Connect</a> with only the  <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_connection_mode">MBN_CONNECTION_MODE_TMP_PROFILE</a><i>connectionMode</i> and the <i>strProfile</i> parameter set to an XML representation of the profile. This implies that the connection is of a temporary nature and not saved for future use by the system.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a>