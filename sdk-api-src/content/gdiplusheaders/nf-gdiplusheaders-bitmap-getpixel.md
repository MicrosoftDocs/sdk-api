---
UID: NF:gdiplusheaders.Bitmap.GetPixel
title: Bitmap::GetPixel
author: windows-sdk-content
description: The Bitmap::GetPixel method gets the color of a specified pixel in this bitmap.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetPixel_x_y_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\getpixel.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Bitmap class [GDI+],GetPixel method, Bitmap.GetPixel, Bitmap::GetPixel, GetPixel, GetPixel method [GDI+], GetPixel method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetPixel_x_y_color_, gdiplus._gdiplus_CLASS_Bitmap_GetPixel_x_y_color_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.GetPixel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::GetPixel


## -description


The <b>Bitmap::GetPixel</b> method gets the color of a specified pixel in this bitmap.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate (column) of the pixel. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate (row) of the pixel. 


### -param color [out]

Type: <b><a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that receives the color of the specified pixel. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Depending on the format of the bitmap, <b>Bitmap::GetPixel</b> might not return the same value as was set by <a href="https://msdn.microsoft.com/2f5baa4b-f16b-4802-a07a-bd94b7b35c89">Bitmap::SetPixel</a>. For example, if you call <b>Bitmap::SetPixel</b> on a 
				<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object whose pixel format is 32bppPARGB, the pixel's RGB components are premultiplied. A subsequent call to <b>Bitmap::GetPixel</b> might return a different value because of rounding. Also, if you call <b>Bitmap::SetPixel</b> on a 
				<b>Bitmap</b> object whose color depth is 16 bits per pixel, information could be lost during the conversion from 32 to 16 bits, and a subsequent call to <b>Bitmap::GetPixel</b> might return a different value.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object based on a JPEG file. The code calls the <b>Bitmap::GetPixel</b> method to obtain the color of a pixel in the bitmap and then fills a rectangle with the retrieved color.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetPixel(HDC hdc)

{

   Graphics graphics(hdc);

   // Create a Bitmap object from a JPEG file.
   Bitmap myBitmap(L"Climber.jpg");

   // Get the value of a pixel from myBitmap.
   Color pixelColor;
   myBitmap.GetPixel(25, 25, &amp;pixelColor);

   // Fill a rectangle with the pixel color.
   SolidBrush brush(pixelColor);
   graphics.FillRectangle(&amp;brush, Rect(0, 0, 100, 100));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a>



<a href="https://msdn.microsoft.com/2f5baa4b-f16b-4802-a07a-bd94b7b35c89">Bitmap::SetPixel</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

