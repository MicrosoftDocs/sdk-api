---
UID: NF:gdiplusgraphics.Graphics.DrawImage(INImage,INREAL,INREAL,INREAL,INREAL,INREAL,INREAL,INUnit)
title: Graphics::DrawImage(IN Image,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image.
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN Unit)","Graphics.DrawImage(Image*","REAL","REAL","REAL","REAL","REAL","REAL","Unit)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN Unit)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_REAL_x_REAL_y_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_s","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_REAL_x_REAL_y_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_s"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_REAL_x_REAL_y_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_s.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_44imageimage_realx_realy_realsrcx_realsr.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit), Graphics.DrawImage(Image*,REAL,REAL,REAL,REAL,REAL,REAL,Unit), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit), _gdiplus_CLASS_Graphics_DrawImage_Image_image_REAL_x_REAL_y_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_s, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_REAL_x_REAL_y_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_s
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

# Graphics::DrawImage(IN Image,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit)


## -description

The <b>Graphics::DrawImage</b> method draws an image.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the source image.

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the destination position at which to draw the image.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the destination position at which to draw the image.

### -param srcx [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the portion of the source image to be drawn.

### -param srcy [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the portion of the source image to be drawn.

### -param srcwidth [in]

Type: <b>REAL</b>

Real number that specifies the width of the portion of the source image to be drawn.

### -param srcheight [in]

Type: <b>REAL</b>

Real number that specifies the height of the portion of the source image to be drawn.

### -param srcUnit [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for the image. The default value is UnitPixel.

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