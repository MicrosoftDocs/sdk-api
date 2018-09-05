---
UID: NN:upnphost.IUPnPDeviceProvider
title: IUPnPDeviceProvider
author: windows-sdk-content
description: The IUPnPDeviceProvider interface allows a device provider to start and stop its processing.
old-location: upnp\iupnpdeviceprovider.htm
old-project: UPnP
ms.assetid: daaa8b55-bcef-4142-8f7b-e6f64e0ac258
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPDeviceProvider, IUPnPDeviceProvider interface [UPnP APIs], IUPnPDeviceProvider interface [UPnP APIs],described, _upnp_iupnpdeviceprovider, upnp.iupnpdeviceprovider, upnphost/IUPnPDeviceProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnphost.h
req.include-header: 
req.redist: 
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
 - IUPnPDeviceProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceProvider interface


## -description


The 
<b>IUPnPDeviceProvider</b> interface allows a device provider to start and stop its processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a76c7063-bad5-4f59-a5ca-8a8a4a79787e">Start</a>
</td>
<td align="left" width="63%">
Method that is called by the device host when the device provider should start its processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8e4cd95-a6dc-4bf9-921e-63fbac743028">Stop</a>
</td>
<td align="left" width="63%">
Method that is called by the device host when the device provider should stops its processing.

</td>
</tr>
</table> 

