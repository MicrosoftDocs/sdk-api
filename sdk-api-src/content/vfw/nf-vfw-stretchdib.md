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

# StretchDIB function


## -description



The <b>StretchDIB</b> function copies a device independent bitmap from one memory location to another and resizes the image to fit the destination rectangle.




## -parameters




### -param biDst

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure that describes the destination bitmap.


### -param lpDst

TBD


### -param DstX

X coordinate of the destination rectangle's origin.


### -param DstY

Y coordinate of the destination rectangle's origin.


### -param DstXE

Width, in pixels, of the destination rectangle.


### -param DstYE

Height, in pixels, of the destination rectangle.


### -param biSrc

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure that describes the source bitmap.


### -param lpSrc

TBD


### -param SrcX

X coordinate of the source rectangle's origin.


### -param SrcY

Y coordinate of the source rectangle's origin.


### -param SrcXE

Width, in pixels, of the source rectangle.


### -param SrcYE

Height, in pixels, of the source rectangle.


#### - lpvDst

Pointer to the memory buffer that will receive the copied pixel bits.


#### - lpvSrc

Pointer to the source bitmap data.


## -returns



This function does not return a value.




## -remarks



The size of the destination buffer must be large enough to accommodate any alignment bytes at the end of each pixel row.

This function does nothing if <i>biSrc</i> and <i>biDst</i> have different values for <i>biBitCount</i> or if the value for <i>biSrc</i>.  <i>biBitCount</i> does not equal 8, 16, or 24.

This function performs no dithering or other smoothing. Pixel values are merely dropped or duplicated on a line-by-line, column-by-column basis.

This function does not do any special processing based on pixel encoding except for calculating the number of bits per pixel. In particular this function will not generate correct results when pixels are encoded in groups of more than 1 pixel, as in the case of a YUV format where U and V are decimated and so are not represented equally in each pixel.

Before including Vfw.h, you must add the following line to your code:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define DRAWDIB_INCLUDE_STRETCHDIB
</pre>
</td>
</tr>
</table></span></div>


