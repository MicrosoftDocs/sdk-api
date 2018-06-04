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

# TextureBrush::TextureBrush(IN Image,IN WrapMode,IN INT,IN INT,IN INT,IN INT)


## -description


<span>This topic lists the constructors of the 
			<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> class. For a complete class listing, see <b>TextureBrush Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6197576-4e78-4a20-b7be-e01da179b08f">TextureBrush(Image*,WrapMode)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image and a wrap mode. The size of the brush defaults to the size of the image, so the entire image is used by the brush.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e38397a-2308-4108-bf69-f3d3035dee8d">TextureBrush(Image*,WrapMode,Rect&)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f710eab-81fb-4c43-810f-1ead3c9b2510">TextureBrush(Image*,wrapMode,RectF&)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2013c6-8810-4592-83be-354f8f46be89">TextureBrush(Image*,Rect&,ImageAttributes*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a defining rectangle, and a set of image properties.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff10237-99fe-41c7-b051-2da96869f1a6">TextureBrush(Image*,RectF&,ImageAttributes*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a defining rectangle, and a set of image properties.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5056797a-970a-469f-a80f-38182aca55e0">TextureBrush(Image*,WrapMode,INT,INT,INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining set of coordinates.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f955c5c-8a32-4fec-a26a-67a0d2cb9ac7">TextureBrush(Image*,WrapMode,REAL,REAL,REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining set of coordinates.

</td>
</tr>
</table>

## -parameters

