---
UID: NN:mswmdm.IWMDMEnumDevice
title: IWMDMEnumDevice (mswmdm.h)
author: windows-sdk-content
description: The IWMDMEnumDevice interface enumerates portable devices attached to a computer. To obtain this interface, call IWMDeviceManager::EnumDevices.
old-location: wmdm\iwmdmenumdevice.htm
tech.root: WMDM
ms.assetid: fcb93d2a-2107-4aa9-9b3a-130044d7dc96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMEnumDevice, IWMDMEnumDevice interface [windows Media Device Manager], IWMDMEnumDevice interface [windows Media Device Manager],described, IWMDMEnumDeviceInterface, mswmdm/IWMDMEnumDevice, wmdm.iwmdmenumdevice
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMEnumDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/c8118950-d96f-4720-ab3a-f5ea93065875">Clone</a>
</td>
<td align="left" width="63%">
Returns a copy of the <b>IWMDMEnumDevice</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75a5961f-2c61-4e10-a570-7ebfabb97367">Next</a>
</td>
<td align="left" width="63%">
Returns a pointer to the next device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af06bc07-2043-4ef5-a1f2-381797fb750b">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration so that <b>Next</b> returns a pointer to the first device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd6d2066-5445-4e29-812f-7d52dc67d57a">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of devices in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

