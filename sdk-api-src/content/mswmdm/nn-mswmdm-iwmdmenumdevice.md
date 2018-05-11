---
UID: NN:mswmdm.IWMDMEnumDevice
title: IWMDMEnumDevice
author: windows-driver-content
description: The IWMDMEnumDevice interface enumerates portable devices attached to a computer. To obtain this interface, call IWMDeviceManager::EnumDevices.
old-location: wmdm\iwmdmenumdevice.htm
old-project: WMDM
ms.assetid: fcb93d2a-2107-4aa9-9b3a-130044d7dc96
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMDMEnumDevice, IWMDMEnumDevice interface [windows Media Device Manager], IWMDMEnumDevice interface [windows Media Device Manager],described, IWMDMEnumDeviceInterface, mswmdm/IWMDMEnumDevice, wmdm.iwmdmenumdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IWMDMEnumDevice
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMEnumDevice interface


## -description



The <b>IWMDMEnumDevice</b> interface enumerates portable devices attached to a computer. To obtain this interface, call <a href="https://msdn.microsoft.com/1daa6d36-9858-4504-a9a2-c0341031829b">IWMDeviceManager::EnumDevices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMEnumDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMEnumDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMEnumDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Returns a copy of the <b>IWMDMEnumDevice</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Returns a pointer to the next device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration so that <b>Next</b> returns a pointer to the first device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of devices in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

