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

# Region::Union(IN const Region)


## -description


<span>This topic lists the 
			Union methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a> class. For a complete list of methods for the <b>Region</b> class, see <a href="https://msdn.microsoft.com/bbaa4027-94aa-497f-8efb-a82d251847af">Region Methods</a>. 

</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dde2ebc1-cb66-41ac-81ef-5ef53f427ed7">Union(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/dde2ebc1-cb66-41ac-81ef-5ef53f427ed7">Region::Union</a> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified rectangle's interior.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3320ee60-c7ba-498d-aeee-cb947aaec2bb">Union(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3320ee60-c7ba-498d-aeee-cb947aaec2bb">Region::Union</a> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified rectangle's interior.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ab6000c-02d9-46b7-8ec0-7ece83bf2a09">Union(Region*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8ab6000c-02d9-46b7-8ec0-7ece83bf2a09">Region::Union</a> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of another region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5f13ab5-7013-4c17-b8fa-304bf15235be">Union(GraphicsPath*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e5f13ab5-7013-4c17-b8fa-304bf15235be">Region::Union</a> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified path's interior.

</td>
</tr>
</table>

## -parameters

