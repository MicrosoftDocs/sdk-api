---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(Image,WrapMode,INT,INT,INT,INT)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode,IN INT,IN INT,IN INT,IN INT) (gdiplusbrush.h)
description: Creates a TextureBrush object based on an image, a wrap mode, and a defining set of coordinates. (overload 1/2)
helpviewer_keywords: ["TextureBrush","TextureBrush class [GDI+]","TextureBrush constructor","TextureBrush constructor [GDI+]","TextureBrush constructor [GDI+]","TextureBrush class","TextureBrush.TextureBrush","TextureBrush.TextureBrush(IN Image","IN WrapMode","IN INT","IN INT","IN INT","IN INT)","TextureBrush.TextureBrush(Image*","WrapMode","INT","INT","INT","INT)","TextureBrush::TextureBrush","TextureBrush::TextureBrush(IN Image","IN WrapMode","IN INT","IN INT","IN INT","IN INT)","_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_INT_dstX_INT_dstY_INT_dstWidt","gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_INT_dstX_INT_dstY_INT_dstWidt"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_INT_dstX_INT_dstY_INT_dstWidt.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_29imageimage_wrapmodewrapmode_intdstx_in.htm
ms.date: 12/05/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode,IN INT,IN INT,IN INT,IN INT), TextureBrush.TextureBrush(Image*,WrapMode,INT,INT,INT,INT), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_INT_dstX_INT_dstY_INT_dstWidt, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_INT_dstX_INT_dstY_INT_dstWidt
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

# TextureBrush::TextureBrush(IN Image,IN WrapMode,IN INT,IN INT,IN INT,IN INT)


## -description

Creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object based on an image, a wrap mode, and a defining set of coordinates.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that contains the bitmap of the image to use.

### -param wrapMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush.

### -param dstX [in]

Type: <b>INT</b>

Leftmost coordinate of the image portion to be used by this brush.

### -param dstY [in]

Type: <b>INT</b>

Uppermost coordinate of the image portion to be used by this brush.

### -param dstWidth [in]

Type: <b>INT</b>

Width of the brush and width of the image portion to be used by the brush.

### -param dstHeight [in]

Type: <b>INT</b>

Height of the brush and height of the image portion to be used by the brush.

## -remarks

The 
				<i>dstX</i>, 
				<i>dstY</i>, 
				<i>dstWidth</i>, and 
				<i>dstHeight</i> parameters specify a rectangle. The size of the brush is defined by 
				<i>dstWidth</i> and 
				<i>dstHeight</i>. The 
				<i>dstX</i> and 
				<i>dstY</i> parameters have no effect on the brush's size or position — the brush is always oriented at (0, 0). The 
				<i>dstX</i>, 
				<i>dstY</i>, 
				<i>dstWidth</i>, and 
				<i>dstHeight</i> parameters define the portion of the image to be used by the brush.

For example, suppose you have an image that is stored in an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object and is 256
				×512 (width
				×height) pixels. Then you create a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object based on this image as follows:

<code>TextureBrush(&amp;someImage, WrapModeTile, 12, 50, 100, 150)</code>

The brush will have a width of 100 units and a height of 150 units. The brush will use a rectangular portion of the image. This portion begins at the pixel having coordinates (12, 50). The width and height of the portion are 100 and 150, respectively, measured from the starting pixel. 

Now suppose you create another <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object based on the same image and specify a different rectangle:

<code>TextureBrush(&amp;someImage, WrapModeTile, 0, 0, 256, 512)</code>

The brush will have width and height equal to 256 and 512, respectively. The brush will use the entire image instead of a portion of it because the rectangle specifies a starting pixel at coordinates (0, 0) and dimensions identical to those of the image.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-getwrapmode">TextureBrush::GetWrapMode</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-setwrapmode">TextureBrush::SetWrapMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>
