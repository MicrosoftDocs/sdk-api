---
UID: NN:mbnapi.IMbnConnection
title: IMbnConnection
author: windows-driver-content
description: Represents the network connectivity of a device.
old-location: mbn\imbnconnection.htm
old-project: mbn
ms.assetid: dae6ce6f-2534-4799-8ed3-53cd1f2eca13
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnConnection, IMbnConnection interface [Microsoft Broadband Networks], IMbnConnection interface [Microsoft Broadband Networks], described, mbn.imbnconnection, mbnapi/IMbnConnection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnection interface


## -description


Represents the network connectivity of a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/66acb84e-8e0f-4ff1-abc4-b32f782ce9f3">Connect</a>
</td>
<td align="left" width="63%">
Establishes a data connection.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc7f28db-499d-41be-a2cc-b4940a5bccd6">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a data connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8bda00b-5eff-46a4-b640-1794e8ea21cf">GetActivationNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error returned in a context activation failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85f3e0bb-c694-4870-b423-cb4ac7a0477d">GetConnectionState</a>
</td>
<td align="left" width="63%">
Gets the current connection state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a715f7c8-a001-41a2-9c1f-ca133568133b">GetVoiceCallState</a>
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

<a href="https://msdn.microsoft.com/c9e24426-a487-417a-947e-6315eb59f9b4">ConnectionID</a>


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

<a href="https://msdn.microsoft.com/c98f1f69-1df1-4d72-8df4-166284dcb880">InterfaceID</a>


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



This interface is only available when a Mobile Broadband device is registered to a network or when the device is in <b>MBN_READY_STATE_DEVICE_LOCKED</b> state. When a device deregisters from the network this COM interface is removed and the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/020ee1ad-cab5-4a27-b97b-160319d84ac8">OnConnectionRemoval</a> method of the <a href="https://msdn.microsoft.com/153ab8c5-2b39-44a7-8c12-9f1df0012270">IMbnConnectionManagerEvents</a> interface.

<b>IMbnConnection</b> objects are provided by calls to the <a href="https://msdn.microsoft.com/fbeac057-77e3-438e-a7a9-b6f223a09dbe">GetConnection</a> and <a href="https://msdn.microsoft.com/5f4fd3b2-ed24-403a-ae5a-31821a2c7033">GetConnections</a> methods of the <a href="https://msdn.microsoft.com/20b9243d-1f20-4092-951a-fbacb2d55481">IMbnConnectionManager</a> interface.  



