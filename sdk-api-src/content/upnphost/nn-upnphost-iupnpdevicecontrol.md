---
UID: NN:upnphost.IUPnPDeviceControl
title: IUPnPDeviceControl
author: windows-sdk-content
description: The IUPnPDeviceControl interface is the central point of management for a device and its service objects.
old-location: upnp\iupnpdevicecontrol.htm
old-project: upnp
ms.assetid: c5d68459-f4ba-4df1-a00c-be86e24ce29f
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IUPnPDeviceControl, IUPnPDeviceControl interface [UPnP APIs], IUPnPDeviceControl interface [UPnP APIs],described, _upnp_iupnpdevicecontrol, upnp.iupnpdevicecontrol, upnphost/IUPnPDeviceControl
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
 - IUPnPDeviceControl
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceControl interface


## -description


The 
<b>IUPnPDeviceControl</b> interface is the central point of management for a device and its service objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55b54edf-fd1d-45b8-95d4-a746a60e5310">GetServiceObject</a>
</td>
<td align="left" width="63%">
Method that returns an <b>IDispatch</b> pointer to the service object that was requested by the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c1ea343-f04b-414d-92cf-044cb117bc9c">Initialize</a>
</td>
<td align="left" width="63%">
Method that initializes the device control object with the device description and a device-specific initialization string.

</td>
</tr>
</table> 

