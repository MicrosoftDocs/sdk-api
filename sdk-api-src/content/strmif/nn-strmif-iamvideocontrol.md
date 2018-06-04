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

# IAMVideoControl interface


## -description



The <b>IAMVideoControl</b> interface controls certain video capture operations such as enumerating available frame rates and image orientation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVideoControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e4b7b46-8179-410c-8369-652f9b65de8c">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the underlying hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/373cabed-af09-4d54-b4e1-0ef87727430a">GetCurrentActualFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the actual frame rate at which the device is streaming. This method is used with devices, such as the Universal Serial Bus (USB) or cameras that use the IEEE 1394 serial standard, where the maximum frame rate can be limited by bandwidth availability. This is only available during video streaming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/864f294f-1a18-4d4c-952e-1965da4c9496">GetFrameRateList</a>
</td>
<td align="left" width="63%">
Retrieves a list of available frame rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a196cf6e-491c-4d01-abfe-831440e75058">GetMaxAvailableFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum frame rate currently available based on bus bandwidth usage for connections such as USB and IEEE 1394 camera devices where the maximum frame rate can be limited by bandwidth availability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b937661-67b2-445c-ab25-8655e1036797">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the video control mode of operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09fe5d3f-41d8-4a60-a770-64c628a6b82d">SetMode</a>
</td>
<td align="left" width="63%">
Sets the video control mode of operation.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568120">PROPSETID_VIDCAP_VIDEOCONTROL</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

