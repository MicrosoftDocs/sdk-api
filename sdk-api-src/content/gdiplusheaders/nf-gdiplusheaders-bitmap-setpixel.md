---
UID: NF:gdiplusheaders.Bitmap.SetPixel
title: Bitmap::SetPixel (gdiplusheaders.h)
description: The Bitmap::SetPixel method sets the color of a specified pixel in this bitmap.
helpviewer_keywords: ["Bitmap class [GDI+]","SetPixel method","Bitmap.SetPixel","Bitmap::SetPixel","SetPixel","SetPixel method [GDI+]","SetPixel method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_SetPixel_x_y_color_","gdiplus._gdiplus_CLASS_Bitmap_SetPixel_x_y_color_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_SetPixel_x_y_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\setpixel.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],SetPixel method, Bitmap.SetPixel, Bitmap::SetPixel, SetPixel, SetPixel method [GDI+], SetPixel method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_SetPixel_x_y_color_, gdiplus._gdiplus_CLASS_Bitmap_SetPixel_x_y_color_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Bitmap::SetPixel
 - gdiplusheaders/Bitmap::SetPixel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.SetPixel
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

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color to set.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Depending on the format of the bitmap, <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel">Bitmap::GetPixel</a> might not return the same value as was set by <b>Bitmap::SetPixel</b>. For example, if you call <b>Bitmap::SetPixel</b> on a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object whose pixel format is 32bppPARGB, the RGB components are premultiplied. A subsequent call to <b>Bitmap::GetPixel</b> might return a different value because of rounding. Also, if you call <b>Bitmap::SetPixel</b> on a 
				<b>Bitmap</b> whose color depth is 16 bits per pixel, information could be lost in the conversion from 32 to 16 bits, and a subsequent call to <b>Bitmap::GetPixel</b> might return a different value.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a JPEG file. The code draws the bitmap once unaltered. Then the code calls the <b>Bitmap::SetPixel</b> method to create a checkered pattern of black pixels in the bitmap and draws the altered bitmap.


```cpp
VOID Example_SetPixel(HDC hdc)

{
   Graphics graphics(hdc);

   // Create a Bitmap object from a JPEG file.
   Bitmap myBitmap(L"Climber.jpg");

   // Draw the bitmap.
   graphics.DrawImage(&myBitmap, 0, 0);

   // Create a checkered pattern with black pixels.
   for (UINT row = 0; row < myBitmap.GetWidth(); row += 2)
   {
      for (UINT col = 0; col < myBitmap.GetHeight(); col += 2)
      {
         myBitmap.SetPixel(row, col, Color(255, 0, 0, 0));
      }
   }

   // Draw the altered bitmap.
   graphics.DrawImage(&myBitmap, 200, 0);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel">Bitmap::GetPixel</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>