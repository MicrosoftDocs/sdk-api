---
UID: NF:gdiplusgraphics.Graphics.DrawImage(Image,constRect&)
title: Graphics::DrawImage(IN Image,IN const Rect &) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image. (overload 11/14)
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN const Rect &)","Graphics.DrawImage(Image*","const Rect&)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN const Rect &)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_rect_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_77imageimage_rectamprect.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const Rect &), Graphics.DrawImage(Image*,const Rect&), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const Rect &), _gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_rect_
req.header: gdiplusgraphics.h
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
 - Graphics::DrawImage
 - gdiplusgraphics/Graphics::DrawImage
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
 - Graphics.DrawImage
---

# Graphics::DrawImage(IN Image,IN const Rect &)


## -description

The <b>Graphics::DrawImage</b> method draws an image.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the source image.

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that bounds the drawing area for the image.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The image is scaled to fit the rectangle.


#### Examples



The following example draws the source image, the rectangle that bounds the resized image, and then draws the resized image to fit the rectangle.


```cpp
VOID Example_DrawImage9(HDC hdc)

{
   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"climber.jpg");

   // Create a Pen object.
   Pen pen (Color(255, 255, 0, 0), 2);

   // Draw the original source image.
   graphics.DrawImage(&image, 10, 10);

   // Create a Rect object that specifies the destination of the image.
   Rect destRect(200, 50, 150, 75);

   // Draw the rectangle that bounds the image.
   graphics.DrawRectangle(&pen, destRect);

   // Draw the image.
   graphics.DrawImage(&image, destRect);
}
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing two versions of the same image; the second is slightly narrower than the first, much shorter, and outlined in red" src="images/drawimage6.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
