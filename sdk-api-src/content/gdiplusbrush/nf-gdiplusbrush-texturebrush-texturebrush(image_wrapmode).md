---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(Image,WrapMode)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode) (gdiplusbrush.h)
description: Creates a TextureBrush object based on an image and a wrap mode. The size of the brush defaults to the size of the image, so the entire image is used by the brush.
helpviewer_keywords: ["TextureBrush","TextureBrush class [GDI+]","TextureBrush constructor","TextureBrush constructor [GDI+]","TextureBrush constructor [GDI+]","TextureBrush class","TextureBrush.TextureBrush","TextureBrush.TextureBrush(IN Image","IN WrapMode)","TextureBrush.TextureBrush(Image*","WrapMode)","TextureBrush::TextureBrush","TextureBrush::TextureBrush(IN Image","IN WrapMode)","_gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_","gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_99image_wrapmode.htm
ms.date: 12/05/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode), TextureBrush.TextureBrush(Image*,WrapMode), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode), _gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_
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

# TextureBrush::TextureBrush(IN Image,IN WrapMode)


## -description

Creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object based on an image and a wrap mode. The size of the brush defaults to the size of the image, so the entire image is used by the brush.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that contains the bitmap of the image to use.

### -param wrapMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. The default value is <b>WrapModeTile</b>.

## -remarks

An area that extends beyond the boundaries of the brush is tiled with repeated copies of the brush. A texture brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the brush's image. For example, if the wrap mode is specified as <b>WrapModeTileFlipX</b>, the brush is flipped about a line that is parallel to the y-axis. 

The texture brush is always oriented at (0, 0). If the wrap mode is specified as <b>WrapModeClamp</b>, no area outside of the brush is tiled. For example, suppose you create a texture brush, specifying <b>WrapModeClamp</b> as the wrap mode:

<code>TextureBrush(&amp;SomeImage, WrapModeClamp)</code>

Then, you paint an area with the brush. If the size of the brush has a height of 50 and the painted area is a rectangle with its upper-left corner at (0, 50), you will see no repeated copies of the brush (no tiling).

The default wrap mode for a texture brush is <b>WrapModeTile</b>, which specifies no flipping of the tile and no clamping.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-getwrapmode">TextureBrush::GetWrapMode</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-setwrapmode">TextureBrush::SetWrapMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>