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

# Graphics::ExcludeClip(IN const Region)


## -description


<span>This topic lists the 
ExcludeClip methods of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class. For a complete list of methods for the 
<b>Graphics</b> class, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>. 


</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c04c1c10-e625-4031-b241-a069668a5285">ExcludeClip(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c04c1c10-e625-4031-b241-a069668a5285">Graphics::ExcludeClip</a> method updates the clipping region to the portion of itself that does not intersect the specified rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3123dbf3-ea4c-4597-abe8-7fb97ec669f5">ExcludeClip(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3123dbf3-ea4c-4597-abe8-7fb97ec669f5">Graphics::ExcludeClip</a> method updates the clipping region to the portion of itself that does not intersect the specified rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b792026-182a-4927-b268-515e3abb41d3">ExcludeClip(Region*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7b792026-182a-4927-b268-515e3abb41d3">Graphics::ExcludeClip</a> method updates the clipping region with the portion of itself that does not overlap the specified region.

</td>
</tr>
</table>

## -parameters

