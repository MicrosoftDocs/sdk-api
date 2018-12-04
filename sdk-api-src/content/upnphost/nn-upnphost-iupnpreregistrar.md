---
UID: NN:upnphost.IUPnPReregistrar
title: IUPnPReregistrar
author: windows-sdk-content
description: The IUPnPReregistrar interface allows the application to re-register a UPnP-based device with the device host.
old-location: upnp\iupnpreregistrar.htm
tech.root: upnp
ms.assetid: e01f325b-8fbd-43f2-a835-41cd3232f62e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUPnPReregistrar, IUPnPReregistrar interface [UPnP APIs], IUPnPReregistrar interface [UPnP APIs],described, _upnp_iupnpreregistrar, upnp.iupnpreregistrar, upnphost/IUPnPReregistrar
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
 - IUPnPReregistrar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPReregistrar interface


## -description


The 
<b>IUPnPReregistrar</b> interface allows the application to re-register a UPnP-based device with the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPReregistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPReregistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPReregistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f8a0a49-49e4-47b9-93bf-ca32cc80e243">ReregisterDevice</a>
</td>
<td align="left" width="63%">
Method that re-registers a non-running device by using the original UDN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5e9257e-1143-416c-8862-a69b726f5e23">ReregisterRunningDevice</a>
</td>
<td align="left" width="63%">
Method that re-registers a running device by using the original UDN.

</td>
</tr>
</table> 

