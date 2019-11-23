---
UID: NN:upnphost.IUPnPDeviceControl
title: IUPnPDeviceControl (upnphost.h)

description: The IUPnPDeviceControl interface is the central point of management for a device and its service objects.
old-location: upnp\iupnpdevicecontrol.htm
tech.root: upnp
ms.assetid: c5d68459-f4ba-4df1-a00c-be86e24ce29f

ms.date: 12/05/2018
ms.keywords: IUPnPDeviceControl, IUPnPDeviceControl interface [UPnP APIs], IUPnPDeviceControl interface [UPnP APIs],described, _upnp_iupnpdevicecontrol, upnp.iupnpdevicecontrol, upnphost/IUPnPDeviceControl
ms.topic: interface
f1_keywords: 
 - "upnphost/IUPnPDeviceControl"
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
 - IUPnPDeviceControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceControl interface


## -description


The 
<b>IUPnPDeviceControl</b> interface is the central point of management for a device and its service objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject">GetServiceObject</a>
</td>
<td align="left" width="63%">
Method that returns an <b>IDispatch</b> pointer to the service object that was requested by the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Method that initializes the device control object with the device description and a device-specific initialization string.

</td>
</tr>
</table> 

