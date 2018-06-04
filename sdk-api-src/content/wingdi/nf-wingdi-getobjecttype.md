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

# GetObjectType function


## -description


The <b>GetObjectType</b> retrieves the type of the specified object.


## -parameters




### -param h [in]

A handle to the graphics object.


## -returns



If the function succeeds, the return value identifies the object. This value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>OBJ_BITMAP</td>
<td>Bitmap</td>
</tr>
<tr>
<td>OBJ_BRUSH</td>
<td>Brush</td>
</tr>
<tr>
<td>OBJ_COLORSPACE</td>
<td>Color space</td>
</tr>
<tr>
<td>OBJ_DC</td>
<td>Device context</td>
</tr>
<tr>
<td>OBJ_ENHMETADC</td>
<td>Enhanced metafile DC</td>
</tr>
<tr>
<td>OBJ_ENHMETAFILE</td>
<td>Enhanced metafile</td>
</tr>
<tr>
<td>OBJ_EXTPEN</td>
<td>Extended pen</td>
</tr>
<tr>
<td>OBJ_FONT</td>
<td>Font</td>
</tr>
<tr>
<td>OBJ_MEMDC</td>
<td>Memory DC</td>
</tr>
<tr>
<td>OBJ_METAFILE</td>
<td>Metafile</td>
</tr>
<tr>
<td>OBJ_METADC</td>
<td>Metafile DC</td>
</tr>
<tr>
<td>OBJ_PAL</td>
<td>Palette</td>
</tr>
<tr>
<td>OBJ_PEN</td>
<td>Pen</td>
</tr>
<tr>
<td>OBJ_REGION</td>
<td>Region</td>
</tr>
</table>
 

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

