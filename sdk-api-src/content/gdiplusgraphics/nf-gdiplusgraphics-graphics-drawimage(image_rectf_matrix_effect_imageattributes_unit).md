---
UID: NF:gdiplusgraphics.Graphics.DrawImage(Image,RectF,Matrix,Effect,ImageAttributes,Unit)
title: Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit) (gdiplusgraphics.h)
description: The method draws a portion of an image after applying a specified effect.
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN RectF","IN Matrix","IN Effect","IN ImageAttributes","IN Unit)","Graphics.DrawImage(Image*","RectF*","Matrix*","Effect*","ImageAttributes*","Unit*)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN RectF","IN Matrix","IN Effect","IN ImageAttributes","IN Unit)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_imageimage_rectfsourcerect_matrixxform.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), Graphics.DrawImage(Image*,RectF*,Matrix*,Effect*,ImageAttributes*,Unit*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_
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

# Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit)


## -description

The  method draws a portion of an image after applying a specified effect.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the image to be drawn.

### -param sourceRect [in]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that specifies the portion of the image to be drawn.

### -param xForm [in]

Type: <b><a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the parallelogram in which the image portion is rendered. The destination parallelogram is calculated by applying the affine transformation stored in the matrix to the source rectangle.

### -param effect [in]

Type: <b><a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>*</b>

Pointer to a instance of a descendant of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a> class. The descendant specifies an effect or adjustment (for example, a change in contrast) that is applied to the image before rendering. The image is not permanently altered by the effect.

### -param imageAttributes [in]

Type: <b><a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object that specifies color adjustments to be applied when the image is rendered. Can be <b>NULL</b>.

### -param srcUnit [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>*</b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for the source rectangle.

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