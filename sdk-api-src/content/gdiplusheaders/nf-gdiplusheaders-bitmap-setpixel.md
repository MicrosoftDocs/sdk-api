---
UID: NF:gdiplusheaders.Bitmap.SetPixel
title: Bitmap::SetPixel
author: windows-sdk-content
description: The Bitmap::SetPixel method sets the color of a specified pixel in this bitmap.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_SetPixel_x_y_color_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\setpixel.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Bitmap class [GDI+],SetPixel method, Bitmap.SetPixel, Bitmap::SetPixel, SetPixel, SetPixel method [GDI+], SetPixel method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_SetPixel_x_y_color_, gdiplus._gdiplus_CLASS_Bitmap_SetPixel_x_y_color_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.SetPixel
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Bitmap::SetPixel


## -description


The <b>Bitmap::SetPixel</b> method sets the color of a specified pixel in this bitmap.


## -parameters




### -param x [in]

Type: <b>INT</b>

<b>int</b> that specifies the x-coordinate (column) of the pixel. 


### -param y [in]

Type: <b>INT</b>

<b>int</b> that specifies the y-coordinate (row) of the pixel. 


### -param color [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color to set. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Depending on the format of the bitmap, <a href="https://msdn.microsoft.com/en-us/library/ms536297(v=VS.85).aspx">Bitmap::GetPixel</a> might not return the same value as was set by <b>Bitmap::SetPixel</b>. For example, if you call <b>Bitmap::SetPixel</b> on a 
				<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object whose pixel format is 32bppPARGB, the RGB components are premultiplied. A subsequent call to <b>Bitmap::GetPixel</b> might return a different value because of rounding. Also, if you call <b>Bitmap::SetPixel</b> on a 
				<b>Bitmap</b> whose color depth is 16 bits per pixel, information could be lost in the conversion from 32 to 16 bits, and a subsequent call to <b>Bitmap::GetPixel</b> might return a different value.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object based on a JPEG file. The code draws the bitmap once unaltered. Then the code calls the <b>Bitmap::SetPixel</b> method to create a checkered pattern of black pixels in the bitmap and draws the altered bitmap.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetPixel(HDC hdc)

{
   Graphics graphics(hdc);

   // Create a Bitmap object from a JPEG file.
   Bitmap myBitmap(L"Climber.jpg");

   // Draw the bitmap.
   graphics.DrawImage(&amp;myBitmap, 0, 0);

   // Create a checkered pattern with black pixels.
   for (UINT row = 0; row &lt; myBitmap.GetWidth(); row += 2)
   {
      for (UINT col = 0; col &lt; myBitmap.GetHeight(); col += 2)
      {
         myBitmap.SetPixel(row, col, Color(255, 0, 0, 0));
      }
   }

   // Draw the altered bitmap.
   graphics.DrawImage(&amp;myBitmap, 200, 0);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536297(v=VS.85).aspx">Bitmap::GetPixel</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

