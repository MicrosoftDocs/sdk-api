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

# CreateCompatibleBitmap function


## -description


The <b>CreateCompatibleBitmap</b> function creates a bitmap compatible with the device that is associated with the specified device context.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param cx

TBD


### -param cy

TBD




#### - nHeight [in]

The bitmap height, in pixels.


#### - nWidth [in]

The bitmap width, in pixels.


## -returns



If the function succeeds, the return value is a handle to the compatible bitmap (DDB).

If the function fails, the return value is <b>NULL</b>.




## -remarks



The color format of the bitmap created by the <b>CreateCompatibleBitmap</b> function matches the color format of the device identified by the <i>hdc</i> parameter. This bitmap can be selected into any memory device context that is compatible with the original device.

Because memory device contexts allow both color and monochrome bitmaps, the format of the bitmap returned by the <b>CreateCompatibleBitmap</b> function differs when the specified device context is a memory device context. However, a compatible bitmap that was created for a nonmemory device context always possesses the same color format and uses the same color palette as the specified device context.

Note: When a memory device context is created, it initially has a 1-by-1 monochrome bitmap selected into it. If this memory device context is used in <b>CreateCompatibleBitmap</b>, the bitmap that is created is a <i>monochrome</i> bitmap. To create a color bitmap, use the <b>HDC</b> that was used to create the memory device context, as shown in the following code:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    HDC memDC = CreateCompatibleDC ( hDC );
    HBITMAP memBM = CreateCompatibleBitmap ( hDC, nWidth, nHeight );
    SelectObject ( memDC, memBM );
</pre>
</td>
</tr>
</table></span></div>
If an application sets the <i>nWidth</i> or <i>nHeight</i> parameters to zero, <b>CreateCompatibleBitmap</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.

If a DIB section, which is a bitmap created by the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function, is selected into the device context identified by the <i>hdc</i> parameter, <b>CreateCompatibleBitmap</b> creates a DIB section.

When you no longer need the bitmap, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/ab7d5224-62de-40a8-909f-564f61c45d01">Scaling an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

