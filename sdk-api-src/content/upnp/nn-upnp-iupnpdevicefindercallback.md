---
UID: NN:upnp.IUPnPDeviceFinderCallback
title: IUPnPDeviceFinderCallback (upnp.h)
author: windows-sdk-content
description: The IUPnPDeviceFinderCallback interface allows the UPnP framework to communicate the results of an asynchronous search to an application.
old-location: upnp\iupnpdevicefindercallback.htm
tech.root: upnp
ms.assetid: 02f1220b-d400-469e-8a28-64871f7fcbe2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceFinderCallback, IUPnPDeviceFinderCallback interface [UPnP APIs], IUPnPDeviceFinderCallback interface [UPnP APIs],described, _upnp_iupnpdevicefindercallback, upnp.iupnpdevicefindercallback, upnp/IUPnPDeviceFinderCallback
ms.topic: interface
f1_keywords: 
 - "upnp/IUPnPDeviceFinderCallback"
dev_langs:
 - c++
req.header: upnp.h
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceFinderCallback interface


## -description


The 
<b>IUPnPDeviceFinderCallback</b> interface allows the UPnP framework to communicate the results of an asynchronous search to an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceFinderCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceFinderCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceFinderCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefindercallback-deviceadded">DeviceAdded</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that a device has been added to the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefindercallback-deviceremoved">DeviceRemoved</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that a device has been removed from the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefindercallback-searchcomplete">SearchComplete</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that the initial search for network devices has been completed.

</td>
</tr>
</table> 

