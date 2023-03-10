---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearRemapTable
title: ImageAttributes::ClearRemapTable (gdiplusimageattributes.h)
description: The ImageAttributes::ClearRemapTable method clears the color-remap table for a specified category.
helpviewer_keywords: ["ClearRemapTable","ClearRemapTable method [GDI+]","ClearRemapTable method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearRemapTable method","ImageAttributes.ClearRemapTable","ImageAttributes::ClearRemapTable","_gdiplus_CLASS_ImageAttributes_ClearRemapTable_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearRemapTable_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearRemapTable_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearremaptable.htm
ms.date: 12/05/2018
ms.keywords: ClearRemapTable, ClearRemapTable method [GDI+], ClearRemapTable method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearRemapTable method, ImageAttributes.ClearRemapTable, ImageAttributes::ClearRemapTable, _gdiplus_CLASS_ImageAttributes_ClearRemapTable_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearRemapTable_type_
req.header: gdiplusimageattributes.h
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
 - ImageAttributes::ClearRemapTable
 - gdiplusimageattributes/ImageAttributes::ClearRemapTable
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
 - ImageAttributes.ClearRemapTable
---

# ImageAttributes::ClearRemapTable


## -description

The <b>ImageAttributes::ClearRemapTable</b> method clears the color-remap table for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the remap table is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a remap table for the default category, a different remap table for the bitmap category, and still a different remap table for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a remap table and a gamma value for the default category. If you set the remap table for the pen category by calling <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a>, then the default remap table will not apply to pens. If you later clear the pen remap table by calling <b>ImageAttributes::ClearRemapTable</b>, the pen category will not revert to the default remap table; rather, the pen category will have no remap table. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>