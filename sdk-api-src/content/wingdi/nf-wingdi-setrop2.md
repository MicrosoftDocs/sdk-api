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

# SetROP2 function


## -description


The <b>SetROP2</b> function sets the current foreground mix mode. GDI uses the foreground mix mode to combine pens and interiors of filled objects with the colors already on the screen. The foreground mix mode defines how colors from the brush or pen and the colors in the existing image are to be combined.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param rop2

TBD




#### - fnDrawMode [in]

The mix mode. This parameter can be one of the following values.

<table>
<tr>
<th>Mix mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="R2_BLACK"></a><a id="r2_black"></a><dl>
<dt><b>R2_BLACK</b></dt>
</dl>
</td>
<td width="60%">
Pixel is always 0.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_COPYPEN"></a><a id="r2_copypen"></a><dl>
<dt><b>R2_COPYPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKNOTPEN"></a><a id="r2_masknotpen"></a><dl>
<dt><b>R2_MASKNOTPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the screen and the inverse of the pen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKPEN"></a><a id="r2_maskpen"></a><dl>
<dt><b>R2_MASKPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the pen and the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKPENNOT"></a><a id="r2_maskpennot"></a><dl>
<dt><b>R2_MASKPENNOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the pen and the inverse of the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGENOTPEN"></a><a id="r2_mergenotpen"></a><dl>
<dt><b>R2_MERGENOTPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the screen color and the inverse of the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGEPEN"></a><a id="r2_mergepen"></a><dl>
<dt><b>R2_MERGEPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the pen color and the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGEPENNOT"></a><a id="r2_mergepennot"></a><dl>
<dt><b>R2_MERGEPENNOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the pen color and the inverse of the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOP"></a><a id="r2_nop"></a><dl>
<dt><b>R2_NOP</b></dt>
</dl>
</td>
<td width="60%">
Pixel remains unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOT"></a><a id="r2_not"></a><dl>
<dt><b>R2_NOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTCOPYPEN"></a><a id="r2_notcopypen"></a><dl>
<dt><b>R2_NOTCOPYPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTMASKPEN"></a><a id="r2_notmaskpen"></a><dl>
<dt><b>R2_NOTMASKPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_MASKPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTMERGEPEN"></a><a id="r2_notmergepen"></a><dl>
<dt><b>R2_NOTMERGEPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_MERGEPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTXORPEN"></a><a id="r2_notxorpen"></a><dl>
<dt><b>R2_NOTXORPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_XORPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_WHITE"></a><a id="r2_white"></a><dl>
<dt><b>R2_WHITE</b></dt>
</dl>
</td>
<td width="60%">
Pixel is always 1.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_XORPEN"></a><a id="r2_xorpen"></a><dl>
<dt><b>R2_XORPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors in the pen and in the screen, but not in both.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value specifies the previous mix mode.

If the function fails, the return value is zero.




## -remarks



Mix modes define how GDI combines source and destination colors when drawing with the current pen. The mix modes are binary raster operation codes, representing all possible Boolean functions of two variables, using the binary operations AND, OR, and XOR (exclusive OR), and the unary operation NOT. The mix mode is for raster devices only; it is not available for vector devices.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ca1930e0-f6f4-44c8-979c-f50881f3c225">GetROP2</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

