---
UID: NN:mswmdm.IWMDMDevice3
title: IWMDMDevice3
author: windows-driver-content
description: The IWMDMDevice3 interface extends IWMDMDevice2 by providing methods to query a device for properties, send device I/O controle codes, and also providing upgraded methods to search for storages and retrieve device format capabilities.
old-location: wmdm\iwmdmdevice3.htm
old-project: WMDM
ms.assetid: 29e0ec95-c1ea-4157-b5aa-39d80fff407d
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDMDevice3, IWMDMDevice3 interface [windows Media Device Manager], IWMDMDevice3 interface [windows Media Device Manager], described, IWMDMDevice3Interface, mswmdm/IWMDMDevice3, wmdm.iwmdmdevice3
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
-	IWMDMDevice3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMDevice3 interface


## -description



The <b>IWMDMDevice3</b> interface extends <b>IWMDMDevice2</b> by providing methods to query a device for properties, send device I/O controle codes, and also providing upgraded methods to search for storages and retrieve device format capabilities.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2</a>. <b>IWMDMDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ef6a95d-d4e2-4608-9a02-98b497e1fdbb">DeviceIoControl</a>
</td>
<td align="left" width="63%">
Sends a Device I/O Control (IOCTL) code to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/481e6c2d-4103-4818-9ad4-733629af9f9d">FindStorage</a>
</td>
<td align="left" width="63%">
Finds a storage by its persistent unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/728df998-748b-4c53-b5a6-3a6ccae0d7e4">GetFormatCapability</a>
</td>
<td align="left" width="63%">
Retrieves device support for files of a specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1c8406f-f0cb-4def-bc26-399908ecbf83">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a specific device metadata property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39483d9a-0725-45fa-9d41-dbabd400b3bf">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a specific device property, if it is writable.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>



<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

