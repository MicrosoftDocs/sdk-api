---
UID: NN:upnphost.IUPnPDeviceProvider
title: IUPnPDeviceProvider (upnphost.h)
author: windows-sdk-content
description: The IUPnPDeviceProvider interface allows a device provider to start and stop its processing.
old-location: upnp\iupnpdeviceprovider.htm
tech.root: upnp
ms.assetid: daaa8b55-bcef-4142-8f7b-e6f64e0ac258
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceProvider, IUPnPDeviceProvider interface [UPnP APIs], IUPnPDeviceProvider interface [UPnP APIs],described, _upnp_iupnpdeviceprovider, upnp.iupnpdeviceprovider, upnphost/IUPnPDeviceProvider
ms.topic: interface
f1_keywords: 
 - "upnphost/IUPnPDeviceProvider"
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
 - IUPnPDeviceProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceProvider interface


## -description


The 
<b>IUPnPDeviceProvider</b> interface allows a device provider to start and stop its processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpdeviceprovider-start">Start</a>
</td>
<td align="left" width="63%">
Method that is called by the device host when the device provider should start its processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpdeviceprovider-stop">Stop</a>
</td>
<td align="left" width="63%">
Method that is called by the device host when the device provider should stops its processing.

</td>
</tr>
</table> 

