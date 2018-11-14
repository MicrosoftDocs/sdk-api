---
UID: NN:upnp.IUPnPHttpHeaderControl
title: IUPnPHttpHeaderControl
author: windows-sdk-content
description: Enables the caller to specify additional HTTP headers sent in HTTP requests to a device.
old-location: upnp\iupnphttpheadercontrol.htm
tech.root: UPnP
ms.assetid: aed33117-9bfd-4a23-998f-4b8d040d6e3b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPHttpHeaderControl, IUPnPHttpHeaderControl interface [UPnP APIs], IUPnPHttpHeaderControl interface [UPnP APIs],described, upnp.iupnphttpheadercontrol, upnp/IUPnPHttpHeaderControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IUPnPHttpHeaderControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPHttpHeaderControl interface


## -description


The <b>IUPnPHttpHeaderControl</b> interface enables the caller to specify additional HTTP headers sent in HTTP requests to a device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPHttpHeaderControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPHttpHeaderControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPHttpHeaderControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e44f83de-eaf6-4b16-a70e-64f4daffc6b3">AddRequestHeaders</a>
</td>
<td align="left" width="63%">
Adds the supplied HTTP header to an HTTP request.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling QueryInterface on the same object that provides an implementation of the <a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a> or <a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a> interfaces, after which <a href="https://msdn.microsoft.com/e44f83de-eaf6-4b16-a70e-64f4daffc6b3">AddRequestHeaders</a> can be called on it.




## -see-also




<a href="https://msdn.microsoft.com/6f73bf8c-0423-430f-a654-58d076712aae">Control Point API Reference</a>



<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>
 

 

