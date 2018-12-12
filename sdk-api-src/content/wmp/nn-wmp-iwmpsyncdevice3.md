---
UID: NN:wmp.IWMPSyncDevice3
title: IWMPSyncDevice3
author: windows-sdk-content
description: The IWMPSyncDevice3 interface provides methods for estimating the size required to synchronize a playlist to a device.
old-location: wmp\iwmpsyncdevice3.htm
tech.root: WMP
ms.assetid: 4fc8d307-38d4-4f46-bd8c-b05d60d9d0fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSyncDevice3, IWMPSyncDevice3 interface [Windows Media Player], IWMPSyncDevice3 interface [Windows Media Player],described, wmp.iwmpsyncdevice3, wmp/IWMPSyncDevice3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPSyncDevice3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSyncDevice3 interface


## -description


The <b>IWMPSyncDevice3</b> interface provides methods for estimating the size required to synchronize a playlist to a device.

To use this interface, you must create a remoted instance of the Windows Media Player 12 control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd563710(v=VS.85).aspx">IWMPSyncDevice2</a>. <b>IWMPSyncDevice3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563714(v=VS.85).aspx">cancelEstimation</a>
</td>
<td align="left" width="63%">
Cancels an estimation that was previously initiated by <a href="https://msdn.microsoft.com/en-us/library/Dd563715(v=VS.85).aspx">estimateSyncSize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563715(v=VS.85).aspx">estimateSyncSize</a>
</td>
<td align="left" width="63%">
Initiates the estimation of the size required on the device to synchronize a specified playlist.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563710(v=VS.85).aspx">IWMPSyncDevice2</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

