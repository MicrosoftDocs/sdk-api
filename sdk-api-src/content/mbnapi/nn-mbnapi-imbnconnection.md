---
UID: NN:mbnapi.IMbnConnection
title: IMbnConnection (mbnapi.h)
description: Represents the network connectivity of a device.helpviewer_keywords: ["IMbnConnection","IMbnConnection interface [Microsoft Broadband Networks]","IMbnConnection interface [Microsoft Broadband Networks]","described","mbn.imbnconnection","mbnapi/IMbnConnection"]
old-location: mbn\imbnconnection.htm
tech.root: mbn
ms.assetid: dae6ce6f-2534-4799-8ed3-53cd1f2eca13
ms.date: 12/05/2018
ms.keywords: IMbnConnection, IMbnConnection interface [Microsoft Broadband Networks], IMbnConnection interface [Microsoft Broadband Networks],described, mbn.imbnconnection, mbnapi/IMbnConnection
f1_keywords:
- mbnapi/IMbnConnection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnection interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Represents the network connectivity of a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-connect">Connect</a>
</td>
<td align="left" width="63%">
Establishes a data connection.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a data connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-getactivationnetworkerror">GetActivationNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error returned in a context activation failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-getconnectionstate">GetConnectionState</a>
</td>
<td align="left" width="63%">
Gets the current connection state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-getvoicecallstate">GetVoiceCallState</a>
</td>
<td align="left" width="63%">
Gets the voice call state of the device.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-get_connectionid">ConnectionID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnection-get_interfaceid">InterfaceID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The interface ID.

</td>
</tr>
</table> 


## -remarks



This interface is only available when a Mobile Broadband device is registered to a network or when the device is in <b>MBN_READY_STATE_DEVICE_LOCKED</b> state. When a device deregisters from the network this COM interface is removed and the Mobile Broadband service will call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanagerevents-onconnectionremoval">OnConnectionRemoval</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a> interface.

<b>IMbnConnection</b> objects are provided by calls to the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnection">GetConnection</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnections">GetConnections</a> methods of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanager">IMbnConnectionManager</a> interface.  



