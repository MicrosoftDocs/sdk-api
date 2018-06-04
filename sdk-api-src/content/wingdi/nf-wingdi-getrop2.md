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

# GetROP2 function


## -description


The <b>GetROP2</b> function retrieves the foreground mix mode of the specified device context. The mix mode specifies how the pen or interior color and the color already on the screen are combined to yield a new color.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value specifies the foreground mix mode.

If the function fails, the return value is zero.




## -remarks



Following are the foreground mix modes.

<table>
<tr>
<th>Mix mode</th>
<th>Description</th>
</tr>
<tr>
<td>R2_BLACK</td>
<td>Pixel is always 0.</td>
</tr>
<tr>
<td>R2_COPYPEN</td>
<td>Pixel is the pen color.</td>
</tr>
<tr>
<td>R2_MASKNOTPEN</td>
<td>Pixel is a combination of the colors common to both the screen and the inverse of the pen.</td>
</tr>
<tr>
<td>R2_MASKPEN</td>
<td>Pixel is a combination of the colors common to both the pen and the screen.</td>
</tr>
<tr>
<td>R2_MASKPENNOT</td>
<td>Pixel is a combination of the colors common to both the pen and the inverse of the screen.</td>
</tr>
<tr>
<td>R2_MERGENOTPEN</td>
<td>Pixel is a combination of the screen color and the inverse of the pen color.</td>
</tr>
<tr>
<td>R2_MERGEPEN</td>
<td>Pixel is a combination of the pen color and the screen color.</td>
</tr>
<tr>
<td>R2_MERGEPENNOT</td>
<td>Pixel is a combination of the pen color and the inverse of the screen color.</td>
</tr>
<tr>
<td>R2_NOP</td>
<td>Pixel remains unchanged.</td>
</tr>
<tr>
<td>R2_NOT</td>
<td>Pixel is the inverse of the screen color.</td>
</tr>
<tr>
<td>R2_NOTCOPYPEN</td>
<td>Pixel is the inverse of the pen color.</td>
</tr>
<tr>
<td>R2_NOTMASKPEN</td>
<td>Pixel is the inverse of the R2_MASKPEN color.</td>
</tr>
<tr>
<td>R2_NOTMERGEPEN</td>
<td>Pixel is the inverse of the R2_MERGEPEN color.</td>
</tr>
<tr>
<td>R2_NOTXORPEN</td>
<td>Pixel is the inverse of the R2_XORPEN color.</td>
</tr>
<tr>
<td>R2_WHITE</td>
<td>Pixel is always 1.</td>
</tr>
<tr>
<td>R2_XORPEN</td>
<td>Pixel is a combination of the colors in the pen and in the screen, but not in both.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/a462a03d-e2c8-403e-aab4-ae03fb96f06f">SetROP2</a>
 

 

