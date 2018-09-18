---
UID: NE:gdipluscolormatrix.ColorMatrixFlags
title: ColorMatrixFlags
author: windows-sdk-content
description: The ColorMatrixFlags enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an ImageAttributes object.
old-location: gdiplus\_gdiplus_ENUM_ColorMatrixFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\colormatrixflags.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: ColorMatrixFlags, ColorMatrixFlags enumeration [GDI+], ColorMatrixFlagsAltGray, ColorMatrixFlagsDefault, ColorMatrixFlagsSkipGrays, _gdiplus_ENUM_ColorMatrixFlags, gdiplus._gdiplus_ENUM_ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlagsAltGray, gdipluscolormatrix/ColorMatrixFlagsDefault, gdipluscolormatrix/ColorMatrixFlagsSkipGrays
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ColorMatrixFlags enumeration


## -description


The <b>ColorMatrixFlags</b> enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an 
			<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object.


## -enum-fields




### -field ColorMatrixFlagsDefault

Specifies that all color values (including grays) are adjusted by the same color-adjustment matrix. 


### -field ColorMatrixFlagsSkipGrays

Specifies that colors are adjusted but gray shades are not adjusted. A gray shade is any color that has the same value for its red, green, and blue components. 


### -field ColorMatrixFlagsAltGray

Specifies that colors are adjusted by one matrix and gray shades are adjusted by another matrix. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535416(v=VS.85).aspx">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535417(v=VS.85).aspx">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535430(v=VS.85).aspx">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535431(v=VS.85).aspx">ImageAttributes::SetColorMatrix</a>
 

 

