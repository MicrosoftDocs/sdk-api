---
UID: NE:gdipluscolormatrix.ColorAdjustType
title: ColorAdjustType (gdipluscolormatrix.h)
description: The ColorAdjustType enumeration specifies which GDI+ objects use color-adjustment information.
helpviewer_keywords: ["ColorAdjustType","ColorAdjustType enumeration [GDI+]","ColorAdjustTypeAny","ColorAdjustTypeBitmap","ColorAdjustTypeBrush","ColorAdjustTypeCount","ColorAdjustTypeDefault","ColorAdjustTypePen","ColorAdjustTypeText","_gdiplus_ENUM_ColorAdjustType","gdiplus._gdiplus_ENUM_ColorAdjustType","gdipluscolormatrix/ColorAdjustType","gdipluscolormatrix/ColorAdjustTypeAny","gdipluscolormatrix/ColorAdjustTypeBitmap","gdipluscolormatrix/ColorAdjustTypeBrush","gdipluscolormatrix/ColorAdjustTypeCount","gdipluscolormatrix/ColorAdjustTypeDefault","gdipluscolormatrix/ColorAdjustTypePen","gdipluscolormatrix/ColorAdjustTypeText"]
old-location: gdiplus\_gdiplus_ENUM_ColorAdjustType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\coloradjusttype.htm
ms.date: 12/05/2018
ms.keywords: ColorAdjustType, ColorAdjustType enumeration [GDI+], ColorAdjustTypeAny, ColorAdjustTypeBitmap, ColorAdjustTypeBrush, ColorAdjustTypeCount, ColorAdjustTypeDefault, ColorAdjustTypePen, ColorAdjustTypeText, _gdiplus_ENUM_ColorAdjustType, gdiplus._gdiplus_ENUM_ColorAdjustType, gdipluscolormatrix/ColorAdjustType, gdipluscolormatrix/ColorAdjustTypeAny, gdipluscolormatrix/ColorAdjustTypeBitmap, gdipluscolormatrix/ColorAdjustTypeBrush, gdipluscolormatrix/ColorAdjustTypeCount, gdipluscolormatrix/ColorAdjustTypeDefault, gdipluscolormatrix/ColorAdjustTypePen, gdipluscolormatrix/ColorAdjustTypeText
req.header: gdipluscolormatrix.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ColorAdjustType
 - gdipluscolormatrix/ColorAdjustType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluscolormatrix.h
api_name:
 - ColorAdjustType
---

# ColorAdjustType enumeration


## -description

The <b>ColorAdjustType</b> enumeration specifies which GDI+ objects use color-adjustment information. You can adjust the colors in a rendered image by passing the address of an 
			<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object to the 
			<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)">Graphics::DrawImage</a> method. An 
			<b>ImageAttributes</b> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. Several of the methods of the 
			<b>ImageAttributes</b> class receive an element of the <b>ColorAdjustType</b> enumeration to specify the adjustment category.

## -enum-fields

### -field ColorAdjustTypeDefault

Specifies that color or grayscale adjustment applies to all categories that do not have adjustment settings of their own.

### -field ColorAdjustTypeBitmap

Specifies that color or grayscale adjustment applies to bitmapped images.

### -field ColorAdjustTypeBrush

Specifies that color or grayscale adjustment applies to brush operations in metafiles.

### -field ColorAdjustTypePen

Specifies that color or grayscale adjustment applies to pen operations in metafiles.

### -field ColorAdjustTypeText

Specifies that color or grayscale adjustment applies to text drawn in metafiles.

### -field ColorAdjustTypeCount

Used internally to record the number of color adjustment types.

### -field ColorAdjustTypeAny

Reserved