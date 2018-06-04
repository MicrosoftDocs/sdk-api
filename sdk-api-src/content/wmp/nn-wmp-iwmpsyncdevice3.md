---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMPSyncDevice3 interface


## -description


The <b>IWMPSyncDevice3</b> interface provides methods for estimating the size required to synchronize a playlist to a device.

To use this interface, you must create a remoted instance of the Windows Media Player 12 control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/b47fc5ea-741d-4e47-baad-afeb659f1079">IWMPSyncDevice2</a>. <b>IWMPSyncDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82e87e44-0a38-43c0-bbed-011581ae8a85">cancelEstimation</a>
</td>
<td align="left" width="63%">
Cancels an estimation that was previously initiated by <a href="https://msdn.microsoft.com/49b07233-df9d-4fd0-836e-62b992408018">estimateSyncSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49b07233-df9d-4fd0-836e-62b992408018">estimateSyncSize</a>
</td>
<td align="left" width="63%">
Initiates the estimation of the size required on the device to synchronize a specified playlist.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b47fc5ea-741d-4e47-baad-afeb659f1079">IWMPSyncDevice2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

