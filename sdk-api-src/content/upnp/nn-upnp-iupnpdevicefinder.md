---
UID: NN:upnp.IUPnPDeviceFinder
title: IUPnPDeviceFinder (upnp.h)
author: windows-sdk-content
description: The IUPnPDeviceFinder interface enables an application to find a device.
old-location: upnp\iupnpdevicefinder.htm
tech.root: upnp
ms.assetid: a4697038-8abc-42f2-9381-702fc82af90b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceFinder, IUPnPDeviceFinder interface [UPnP APIs], IUPnPDeviceFinder interface [UPnP APIs],described, _upnp_iupnpdevicefinder, upnp.iupnpdevicefinder, upnp/IUPnPDeviceFinder
ms.topic: interface
f1_keywords: 
 - "upnp/IUPnPDeviceFinder"
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
 - IUPnPDeviceFinder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceFinder interface


## -description


The 
<b>IUPnPDeviceFinder</b> interface enables an application to find a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceFinder</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPDeviceFinder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceFinder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-cancelasyncfind">CancelAsyncFind</a>
</td>
<td align="left" width="63%">
Cancels an asynchronous search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">CreateAsyncFind</a>
</td>
<td align="left" width="63%">
Creates an asynchronous search operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbytype">FindByType</a>
</td>
<td align="left" width="63%">
Searches synchronously for devices by device type or service type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbyudn">FindByUDN</a>
</td>
<td align="left" width="63%">
Searches synchronously for a device by its unique device name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-startasyncfind">StartAsyncFind</a>
</td>
<td align="left" width="63%">
Starts an asynchronous search.

</td>
</tr>
</table> 

