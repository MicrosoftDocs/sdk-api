---
UID: NN:upnp.IUPnPDeviceFinder
title: IUPnPDeviceFinder
author: windows-sdk-content
description: The IUPnPDeviceFinder interface enables an application to find a device.
old-location: upnp\iupnpdevicefinder.htm
old-project: upnp
ms.assetid: a4697038-8abc-42f2-9381-702fc82af90b
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IUPnPDeviceFinder, IUPnPDeviceFinder interface [UPnP APIs], IUPnPDeviceFinder interface [UPnP APIs],described, _upnp_iupnpdevicefinder, upnp.iupnpdevicefinder, upnp/IUPnPDeviceFinder
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
 - IUPnPDeviceFinder
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceFinder interface


## -description


The 
<b>IUPnPDeviceFinder</b> interface enables an application to find a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceFinder</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IUPnPDeviceFinder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d64db4fe-0b0a-430f-b198-dd49ef40b52e">CancelAsyncFind</a>
</td>
<td align="left" width="63%">
Cancels an asynchronous search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">CreateAsyncFind</a>
</td>
<td align="left" width="63%">
Creates an asynchronous search operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fc28829-8802-457b-a1cf-c74834b6651c">FindByType</a>
</td>
<td align="left" width="63%">
Searches synchronously for devices by device type or service type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88d4e004-7df8-45f4-b6ec-9dcf3f0ccfeb">FindByUDN</a>
</td>
<td align="left" width="63%">
Searches synchronously for a device by its unique device name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3189ea47-8cb3-4b95-b88d-7ff72b776e56">StartAsyncFind</a>
</td>
<td align="left" width="63%">
Starts an asynchronous search.

</td>
</tr>
</table> 

