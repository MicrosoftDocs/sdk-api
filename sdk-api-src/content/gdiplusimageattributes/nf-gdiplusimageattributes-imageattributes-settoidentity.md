---
UID: NF:gdiplusimageattributes.ImageAttributes.SetToIdentity
title: ImageAttributes::SetToIdentity (gdiplusimageattributes.h)
description: The ImageAttributes::SetToIdentity method sets the color-adjustment matrix of a specified category to identity matrix.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetToIdentity method","ImageAttributes.SetToIdentity","ImageAttributes::SetToIdentity","SetToIdentity","SetToIdentity method [GDI+]","SetToIdentity method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetToIdentity_type_","gdiplus._gdiplus_CLASS_ImageAttributes_SetToIdentity_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetToIdentity_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\settoidentity.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetToIdentity method, ImageAttributes.SetToIdentity, ImageAttributes::SetToIdentity, SetToIdentity, SetToIdentity method [GDI+], SetToIdentity method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetToIdentity_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetToIdentity_type_
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
 - ImageAttributes::SetToIdentity
 - gdiplusimageattributes/ImageAttributes::SetToIdentity
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
 - ImageAttributes.SetToIdentity
---

# ImageAttributes::SetToIdentity


## -description

The <b>ImageAttributes::SetToIdentity</b> method sets the color-adjustment matrix of a specified category to identity matrix.

## -parameters

### -param type [in]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is set to identity. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>