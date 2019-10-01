---
UID: NN:upnphost.IUPnPRegistrar
title: IUPnPRegistrar (upnphost.h)
author: windows-sdk-content
description: The IUPnPRegistrar interface registers the devices that run in the context of the device host.
old-location: upnp\iupnpregistrar.htm
tech.root: upnp
ms.assetid: c851e102-4f03-4a21-9e62-9b5c60a728f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPRegistrar, IUPnPRegistrar interface [UPnP APIs], IUPnPRegistrar interface [UPnP APIs],described, _upnp_iupnpregistrar, upnp.iupnpregistrar, upnphost/IUPnPRegistrar
ms.topic: interface
f1_keywords: 
 - "upnphost/IUPnPRegistrar"
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
 - IUPnPRegistrar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPRegistrar interface


## -description


The 
<b>IUPnPRegistrar</b> interface registers the devices that run in the context of the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPRegistrar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPRegistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPRegistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename">GetUniqueDeviceName</a>
</td>
<td align="left" width="63%">
Method that retrieves the UDN of a device. This method is re-entrant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerdevice">RegisterDevice</a>
</td>
<td align="left" width="63%">
Method that registers a non-running device with the device host. The device persists across system boots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider">RegisterDeviceProvider</a>
</td>
<td align="left" width="63%">
Method that registers a device provider with the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice">RegisterRunningDevice</a>
</td>
<td align="left" width="63%">
Method that registers a running device with the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdevice">UnregisterDevice</a>
</td>
<td align="left" width="63%">
Method that unregisters the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdeviceprovider">UnregisterDeviceProvider</a>
</td>
<td align="left" width="63%">
Method that unregisters a device provider.

</td>
</tr>
</table> 

