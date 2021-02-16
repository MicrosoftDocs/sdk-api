---
UID: NF:gdiplusgraphics.Graphics.DrawImage(Image,constRectF&,constRectF&,Unit,constImageAttributes)
title: Graphics::DrawImage(IN Image,IN const RectF &,IN const RectF &,IN Unit,IN const ImageAttributes) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws a specified portion of an image at a specified location.
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN const RectF &","IN const RectF &","IN Unit","IN const ImageAttributes)","Graphics.DrawImage(Image*","RectF&","RectF&","Unit","ImageAttributes*)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN const RectF &","IN const RectF &","IN Unit","IN const ImageAttributes)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_RectF_sourceRect_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_RectF_sourceRect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_RectF_sourceRect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_imageimage_rectfdestrect_rectfsourcerect.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const RectF &,IN const RectF &,IN Unit,IN const ImageAttributes), Graphics.DrawImage(Image*,RectF&,RectF&,Unit,ImageAttributes*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const RectF &,IN const RectF &,IN Unit,IN const ImageAttributes), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_RectF_sourceRect_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_RectF_sourceRect_
req.header: gdiplusgraphics.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
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

# Graphics::DrawImage(IN Image,IN const RectF &,IN const RectF &,IN Unit,IN const ImageAttributes)


## -description

The <b>Graphics::DrawImage</b> method draws a specified portion of an image at a specified location.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the image to be drawn.

### -param destRect [in, ref]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Rectangle, measured in pixels, that specifies the bounds of the rendered image. The portion of the image specified by <i>sourceRect</i> is scaled to fill the rectangle specified by <i>destRect</i>.

### -param sourceRect [in, ref]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Rectangle that specifies the portion of the image to be drawn.

### -param srcUnit [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for the source rectangle.

### -param imageAttributes [in]

Type: <b><a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>*</b>

Optional. Pointer to an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object that specifies color adjustments to be applied when the image is rendered. The default value is <b>NULL</b>.

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