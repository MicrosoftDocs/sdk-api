---
UID: NN:upnphost.IUPnPRegistrar
title: IUPnPRegistrar
author: windows-sdk-content
description: The IUPnPRegistrar interface registers the devices that run in the context of the device host.
old-location: upnp\iupnpregistrar.htm
tech.root: upnp
ms.assetid: c851e102-4f03-4a21-9e62-9b5c60a728f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPRegistrar, IUPnPRegistrar interface [UPnP APIs], IUPnPRegistrar interface [UPnP APIs],described, _upnp_iupnpregistrar, upnp.iupnpregistrar, upnphost/IUPnPRegistrar
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPRegistrar interface


## -description


The 
<b>IUPnPRegistrar</b> interface registers the devices that run in the context of the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPRegistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPRegistrar</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dcffee59-8b2f-443c-915f-6d823018eadd">GetUniqueDeviceName</a>
</td>
<td align="left" width="63%">
Method that retrieves the UDN of a device. This method is re-entrant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bb99a42-143b-495a-8b02-efa7ca1d4d29">RegisterDevice</a>
</td>
<td align="left" width="63%">
Method that registers a non-running device with the device host. The device persists across system boots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f91b29-b535-46e7-834f-97f1a46084f7">RegisterDeviceProvider</a>
</td>
<td align="left" width="63%">
Method that registers a device provider with the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b494b7e-4fcc-4de0-bdcc-96c68a5e0688">RegisterRunningDevice</a>
</td>
<td align="left" width="63%">
Method that registers a running device with the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76fca00c-8638-4e2f-8dd1-20b24cde0108">UnregisterDevice</a>
</td>
<td align="left" width="63%">
Method that unregisters the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/548bd520-9c62-4dae-8ae3-94e3683a34f1">UnregisterDeviceProvider</a>
</td>
<td align="left" width="63%">
Method that unregisters a device provider.

</td>
</tr>
</table> 

