---
UID: NF:gdiplusheaders.Bitmap.GetPixel
title: Bitmap::GetPixel (gdiplusheaders.h)
description: The Bitmap::GetPixel method gets the color of a specified pixel in this bitmap.
helpviewer_keywords: ["Bitmap class [GDI+]","GetPixel method","Bitmap.GetPixel","Bitmap::GetPixel","GetPixel","GetPixel method [GDI+]","GetPixel method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_GetPixel_x_y_color_","gdiplus._gdiplus_CLASS_Bitmap_GetPixel_x_y_color_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetPixel_x_y_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\getpixel.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],GetPixel method, Bitmap.GetPixel, Bitmap::GetPixel, GetPixel, GetPixel method [GDI+], GetPixel method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetPixel_x_y_color_, gdiplus._gdiplus_CLASS_Bitmap_GetPixel_x_y_color_
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
 - Bitmap::GetPixel
 - gdiplusheaders/Bitmap::GetPixel
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
 - Bitmap.GetPixel
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

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that receives the color of the specified pixel.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Depending on the format of the bitmap, <b>Bitmap::GetPixel</b> might not return the same value as was set by <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel">Bitmap::SetPixel</a>. For example, if you call <b>Bitmap::SetPixel</b> on a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object whose pixel format is 32bppPARGB, the pixel's RGB components are premultiplied. A subsequent call to <b>Bitmap::GetPixel</b> might return a different value because of rounding. Also, if you call <b>Bitmap::SetPixel</b> on a 
				<b>Bitmap</b> object whose color depth is 16 bits per pixel, information could be lost during the conversion from 32 to 16 bits, and a subsequent call to <b>Bitmap::GetPixel</b> might return a different value.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a JPEG file. The code calls the <b>Bitmap::GetPixel</b> method to obtain the color of a pixel in the bitmap and then fills a rectangle with the retrieved color.


```cpp
VOID Example_GetPixel(HDC hdc)

{

   Graphics graphics(hdc);

   // Create a Bitmap object from a JPEG file.
   Bitmap myBitmap(L"Climber.jpg");

   // Get the value of a pixel from myBitmap.
   Color pixelColor;
   myBitmap.GetPixel(25, 25, &pixelColor);

   // Fill a rectangle with the pixel color.
   SolidBrush brush(pixelColor);
   graphics.FillRectangle(&brush, Rect(0, 0, 100, 100));
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel">Bitmap::SetPixel</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>