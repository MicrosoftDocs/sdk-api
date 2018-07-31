---
UID: NN:upnp.IUPnPDeviceFinderCallback
title: IUPnPDeviceFinderCallback
author: windows-sdk-content
description: The IUPnPDeviceFinderCallback interface allows the UPnP framework to communicate the results of an asynchronous search to an application.
old-location: upnp\iupnpdevicefindercallback.htm
old-project: UPnP
ms.assetid: 02f1220b-d400-469e-8a28-64871f7fcbe2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUPnPDeviceFinderCallback, IUPnPDeviceFinderCallback interface [UPnP APIs], IUPnPDeviceFinderCallback interface [UPnP APIs],described, _upnp_iupnpdevicefindercallback, upnp.iupnpdevicefindercallback, upnp/IUPnPDeviceFinderCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceFinderCallback interface


## -description


The 
<b>IUPnPDeviceFinderCallback</b> interface allows the UPnP framework to communicate the results of an asynchronous search to an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceFinderCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceFinderCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4a61ca43-cbc6-4db2-9706-23cadbae9c3e">DeviceAdded</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that a device has been added to the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ff7bdd-3fdf-4ee4-84c9-e3527988fea2">DeviceRemoved</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that a device has been removed from the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fcce487-1cfb-47ec-9ea1-7df04985d506">SearchComplete</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that the initial search for network devices has been completed.

</td>
</tr>
</table> 

