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

# IWindowsMediaLibrarySharingDeviceProperty interface


## -description


The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface defines methods that provide access to the name and value of an individual property of a media device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDeviceProperty</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/335e3beb-351e-40ad-b065-7058716180d3">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of an individual property of a media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b51b794c-eda6-4afe-8bb2-14896f7b8b81">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of an individual property of a media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface, call the <a href="https://msdn.microsoft.com/32ae77a2-d80e-4295-9fd2-83b1ad7e8c73">GetProperty</a> method or the <a href="https://msdn.microsoft.com/0c679f64-9d7e-4239-8ee0-2aa5de553c58">get_Item</a> method of the <a href="https://msdn.microsoft.com/b975428c-e518-4bc8-a621-193d510661b0">IWindowsMediaLibrarySharingDeviceProperties</a> interface.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/b1508671-fc81-4fcf-a57b-ffbb86b89e73">Windows Media Library Sharing Services</a>
 

 

