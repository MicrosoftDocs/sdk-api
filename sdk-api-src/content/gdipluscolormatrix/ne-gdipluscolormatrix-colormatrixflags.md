---
UID: NE:gdipluscolormatrix.ColorMatrixFlags
title: ColorMatrixFlags (gdipluscolormatrix.h)
author: windows-sdk-content
description: The ColorMatrixFlags enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an ImageAttributes object.
old-location: gdiplus\_gdiplus_ENUM_ColorMatrixFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\colormatrixflags.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorMatrixFlags, ColorMatrixFlags enumeration [GDI+], ColorMatrixFlagsAltGray, ColorMatrixFlagsDefault, ColorMatrixFlagsSkipGrays, _gdiplus_ENUM_ColorMatrixFlags, gdiplus._gdiplus_ENUM_ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlagsAltGray, gdipluscolormatrix/ColorMatrixFlagsDefault, gdipluscolormatrix/ColorMatrixFlagsSkipGrays
ms.topic: enum
f1_keywords: 
 - "gdipluscolormatrix/ColorMatrixFlags"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluscolormatrix.h
api_name:
 - ColorMatrixFlags
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ColorMatrixFlags enumeration


## -description


The <b>ColorMatrixFlags</b> enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object.


## -enum-fields




### -field ColorMatrixFlagsDefault

Specifies that all color values (including grays) are adjusted by the same color-adjustment matrix. 


### -field ColorMatrixFlagsSkipGrays

Specifies that colors are adjusted but gray shades are not adjusted. A gray shade is any color that has the same value for its red, green, and blue components. 


### -field ColorMatrixFlagsAltGray

Specifies that colors are adjusted by one matrix and gray shades are adjusted by another matrix. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolormatrices">ImageAttributes::ClearColorMatrices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolormatrix">ImageAttributes::ClearColorMatrix</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrices">ImageAttributes::SetColorMatrices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix">ImageAttributes::SetColorMatrix</a>
 

 

