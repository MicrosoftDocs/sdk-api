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

# Region::GetRegionScans


## -description


<span>This topic lists the 
			GetRegionScans methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a> class. For a complete list of methods for the <b>Region</b> class, see <a href="https://msdn.microsoft.com/bbaa4027-94aa-497f-8efb-a82d251847af">Region Methods</a>.

</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a34bdc9d-e769-4579-a167-296f6fa77462">GetRegionScans(Matrix*,Rect*,INT*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a34bdc9d-e769-4579-a167-296f6fa77462">Region::GetRegionScans</a> method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bfb4eed-80f8-4a98-a264-1f47c60f58b8">GetRegionScans(Matrix*,RectF*,INT*)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0bfb4eed-80f8-4a98-a264-1f47c60f58b8">Region::GetRegionScans</a> method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.

</td>
</tr>
</table>

## -parameters

