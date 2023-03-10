---
UID: NF:gdiplusgraphics.Graphics.DrawImage(Image,INT,INT,INT,INT)
title: Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image. (overload 14/14)
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN INT","IN INT","IN INT","IN INT)","Graphics.DrawImage(Image*","INT","INT","INT","INT)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN INT","IN INT","IN INT","IN INT)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_62imageimage_intx_inty_intwidth_intheigh.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT), Graphics.DrawImage(Image*,INT,INT,INT,INT), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_
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

# Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT)


## -description

The <b>Graphics::DrawImage</b> method draws an image.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the source image.

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the destination rectangle at which to draw the image.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the destination rectangle at which to draw the image.

### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the destination rectangle at which to draw the image.

### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the destination rectangle at which to draw the image.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>
