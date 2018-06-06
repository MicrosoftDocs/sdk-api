---
UID: NN:upnphost.IUPnPEventSink
title: IUPnPEventSink
author: windows-sdk-content
description: The IUPnPEventSink interface allows a hosted service to send event notifications to the device host.
old-location: upnp\iupnpeventsink.htm
old-project: UPnP
ms.assetid: 431423c9-2873-422d-a28c-c4ef23109114
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: IUPnPEventSink, IUPnPEventSink interface [UPnP APIs], IUPnPEventSink interface [UPnP APIs],described, _upnp_iupnpeventsink, upnp.iupnpeventsink, upnphost/IUPnPEventSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPEventSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPEventSink interface


## -description


The 
<b>IUPnPEventSink</b> interface allows a hosted service to send event notifications to the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb87345e-6a61-48fd-94dc-9a90f756a586">OnStateChanged</a>
</td>
<td align="left" width="63%">
Method that sends the list of <a href="56037091-5761-40ad-8b25-72f85d41466f">dispids</a> for state variables that have changed and their changed values to the device host. The device host then queries the device for the changed values and sends the event to all subscribed control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95792229-287c-43f1-b03a-45aa63a9682f">OnStateChangedSafe</a>
</td>
<td align="left" width="63%">
The version of 
<a href="https://msdn.microsoft.com/bb87345e-6a61-48fd-94dc-9a90f756a586">OnStateChanged</a> method that must be used by developers using programming languages that do not support native arrays, such as Visual Basic.

</td>
</tr>
</table> 

