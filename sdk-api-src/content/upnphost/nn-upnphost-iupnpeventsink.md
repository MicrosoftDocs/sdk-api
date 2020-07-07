---
UID: NN:upnphost.IUPnPEventSink
title: IUPnPEventSink (upnphost.h)
description: The IUPnPEventSink interface allows a hosted service to send event notifications to the device host.
helpviewer_keywords: ["IUPnPEventSink","IUPnPEventSink interface [UPnP APIs]","IUPnPEventSink interface [UPnP APIs]","described","_upnp_iupnpeventsink","upnp.iupnpeventsink","upnphost/IUPnPEventSink"]
old-location: upnp\iupnpeventsink.htm
tech.root: upnp
ms.assetid: 431423c9-2873-422d-a28c-c4ef23109114
ms.date: 12/05/2018
ms.keywords: IUPnPEventSink, IUPnPEventSink interface [UPnP APIs], IUPnPEventSink interface [UPnP APIs],described, _upnp_iupnpeventsink, upnp.iupnpeventsink, upnphost/IUPnPEventSink
f1_keywords:
- upnphost/IUPnPEventSink
dev_langs:
- c++
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
req.lib: 
req.dll: Upnphost.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Upnphost.dll
api_name:
- IUPnPEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPEventSink interface


## -description


The 
<b>IUPnPEventSink</b> interface allows a hosted service to send event notifications to the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPEventSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsink-onstatechanged">OnStateChanged</a>
</td>
<td align="left" width="63%">
Method that sends the list of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/dispid-constants">dispids</a> for state variables that have changed and their changed values to the device host. The device host then queries the device for the changed values and sends the event to all subscribed control points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsink-onstatechangedsafe">OnStateChangedSafe</a>
</td>
<td align="left" width="63%">
The version of 
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsink-onstatechanged">OnStateChanged</a> method that must be used by developers using programming languages that do not support native arrays, such as Visual Basic.

</td>
</tr>
</table> 

