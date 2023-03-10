---
UID: NF:gdiplusimageattributes.ImageAttributes.SetNoOp
title: ImageAttributes::SetNoOp (gdiplusimageattributes.h)
description: The ImageAttributes::SetNoOp method turns off color adjustment for a specified category. You can call ImageAttributes::ClearNoOp to reinstate the color-adjustment settings that were in place before the call to ImageAttributes::SetNoOp.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetNoOp method","ImageAttributes.SetNoOp","ImageAttributes::SetNoOp","SetNoOp","SetNoOp method [GDI+]","SetNoOp method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetNoOp_type_","gdiplus._gdiplus_CLASS_ImageAttributes_SetNoOp_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetNoOp_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setnoop.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetNoOp method, ImageAttributes.SetNoOp, ImageAttributes::SetNoOp, SetNoOp, SetNoOp method [GDI+], SetNoOp method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetNoOp_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetNoOp_type_
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
 - ImageAttributes::SetNoOp
 - gdiplusimageattributes/ImageAttributes::SetNoOp
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
 - ImageAttributes.SetNoOp
---

# ImageAttributes::SetNoOp


## -description

The <b>ImageAttributes::SetNoOp</b> method turns off color adjustment for a specified category. You can call <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearnoop">ImageAttributes::ClearNoOp</a> to reinstate the color-adjustment settings that were in place before the call to <b>ImageAttributes::SetNoOp</b>.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which color correction is turned off. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearnoop">ImageAttributes::ClearNoOp</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-reset">ImageAttributes::Reset</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-settoidentity">ImageAttributes::SetToIdentity</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>