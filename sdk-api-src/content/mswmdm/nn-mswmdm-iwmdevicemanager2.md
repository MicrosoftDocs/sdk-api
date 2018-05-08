---
UID: NN:mswmdm.IWMDeviceManager2
title: IWMDeviceManager2
author: windows-driver-content
description: The IWMDeviceManager2 interface extends IWMDeviceManager interface.
old-location: wmdm\iwmdevicemanager2.htm
old-project: WMDM
ms.assetid: ea4bf623-c93a-4c0f-a84f-e3a979b37d60
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDeviceManager2, IWMDeviceManager2 interface [windows Media Device Manager], IWMDeviceManager2 interface [windows Media Device Manager],described, IWMDeviceManager2Interface, mswmdm/IWMDeviceManager2, wmdm.iwmdevicemanager2
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
-	IWMDeviceManager2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDeviceManager2 interface


## -description



The <b>IWMDeviceManager2</b> interface extends <a href="https://msdn.microsoft.com/cac68821-42fc-4833-bf2e-eec1768869e6">IWMDeviceManager</a> interface. It provides a way of enumerating devices that takes advantage of the Plug and Play (PnP) system that results in better performance and lower memory use. It also enables the application to query for a specific device based on the canonical name of the device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDeviceManager2</b> interface inherits from <a href="https://msdn.microsoft.com/cac68821-42fc-4833-bf2e-eec1768869e6">IWMDeviceManager</a>. <b>IWMDeviceManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDeviceManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5015263-23f2-466f-a89f-26c14f7a2263">EnumDevices2</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface that is used to enumerate portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfa0fe8d-668a-443b-be50-cf1f83362a14">GetDeviceFromCanonicalName</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMDMDevice</b> interface for a device with a specified canonical name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff561022">Reinitialize</a>
</td>
<td align="left" width="63%">
Forces Windows Media Device Manager to rediscover all the Windows Media Device Manager devices

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cac68821-42fc-4833-bf2e-eec1768869e6">IWMDeviceManager</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

