---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(Image,WrapMode,constRectF&)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &) (gdiplusbrush.h)
description: Creates a TextureBrush object based on an image, a wrap mode, and a defining rectangle. (overload 2/2)
helpviewer_keywords: ["TextureBrush","TextureBrush class [GDI+]","TextureBrush constructor","TextureBrush constructor [GDI+]","TextureBrush constructor [GDI+]","TextureBrush class","TextureBrush.TextureBrush","TextureBrush.TextureBrush(IN Image","IN WrapMode","IN const RectF &)","TextureBrush.TextureBrush(Image*","wrapMode","const RectF&)","TextureBrush::TextureBrush","TextureBrush::TextureBrush(IN Image","IN WrapMode","IN const RectF &)","_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_","gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_10imageimage_wrapmodewrapmode_rectfampds.htm
ms.date: 12/05/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode,IN const RectF &), TextureBrush.TextureBrush(Image*,wrapMode,const RectF&), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_
req.header: gdiplusbrush.h
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
 - TextureBrush::TextureBrush
 - gdiplusbrush/TextureBrush::TextureBrush
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
 - TextureBrush.TextureBrush
---

# TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &)


## -description

Creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object based on an image, a wrap mode, and a defining rectangle.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that contains the bitmap of the image to use.

### -param wrapMode [in]

Type: <b>wrapMode</b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush.

### -param dstRect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle that defines the size of this texture brush and the portion of the image to be used by this texture brush. If the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object is created from a metafile, the brush uses the entire image, which is scaled to fit the size of the brush.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-getwrapmode">TextureBrush::GetWrapMode</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-setwrapmode">TextureBrush::SetWrapMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>
