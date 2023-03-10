---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearColorMatrix
title: ImageAttributes::ClearColorMatrix (gdiplusimageattributes.h)
description: The ImageAttributes::ClearColorMatrix method clears the color-adjustment matrix for a specified category.
helpviewer_keywords: ["ClearColorMatrix","ClearColorMatrix method [GDI+]","ClearColorMatrix method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearColorMatrix method","ImageAttributes.ClearColorMatrix","ImageAttributes::ClearColorMatrix","_gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearcolormatrix.htm
ms.date: 12/05/2018
ms.keywords: ClearColorMatrix, ClearColorMatrix method [GDI+], ClearColorMatrix method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearColorMatrix method, ImageAttributes.ClearColorMatrix, ImageAttributes::ClearColorMatrix, _gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_
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
 - ImageAttributes::ClearColorMatrix
 - gdiplusimageattributes/ImageAttributes::ClearColorMatrix
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
 - ImageAttributes.ClearColorMatrix
---

# ImageAttributes::ClearColorMatrix


## -description

The <b>ImageAttributes::ClearColorMatrix</b> method clears the color-adjustment matrix for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 	<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-adjustment matrix for the default category, a different color-adjustment matrix for the bitmap category, and still a different color-adjustment matrix for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a color-adjustment matrix and a gamma value for the default category. If you set a color-adjustment matrix for the pen category by calling <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix">ImageAttributes::SetColorMatrix</a>, then the default color-adjustment matrix will not apply to pens. If you later clear the pen color-adjustment matrix by calling <b>ImageAttributes::ClearColorMatrix</b>, the pen category will not revert to the default adjustment matrix; rather, the pen category will have no adjustment matrix. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolormatrices">ImageAttributes::ClearColorMatrices</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrices">ImageAttributes::SetColorMatrices</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix">ImageAttributes::SetColorMatrix</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-settoidentity">ImageAttributes::SetToIdentity</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>