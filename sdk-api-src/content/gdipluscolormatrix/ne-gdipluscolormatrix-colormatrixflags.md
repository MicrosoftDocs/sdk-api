---
UID: NE:gdipluscolormatrix.ColorMatrixFlags
title: ColorMatrixFlags
author: windows-driver-content
description: The ColorMatrixFlags enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an ImageAttributes object.
old-location: gdiplus\_gdiplus_ENUM_ColorMatrixFlags.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\colormatrixflags.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ColorMatrixFlags, ColorMatrixFlags enumeration [GDI+], ColorMatrixFlagsAltGray, ColorMatrixFlagsDefault, ColorMatrixFlagsSkipGrays, _gdiplus_ENUM_ColorMatrixFlags, gdiplus._gdiplus_ENUM_ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlags, gdipluscolormatrix/ColorMatrixFlagsAltGray, gdipluscolormatrix/ColorMatrixFlagsDefault, gdipluscolormatrix/ColorMatrixFlagsSkipGrays
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdipluscolormatrix.h
api_name:
-	ColorMatrixFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: C_g18030.dll
req.irql: 
req.product: GDI+ 1.0
---

# ColorMatrixFlags enumeration


## -description


The <b>ColorMatrixFlags</b> enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an 
			<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object.


## -enum-fields




### -field ColorMatrixFlagsDefault

Specifies that all color values (including grays) are adjusted by the same color-adjustment matrix. 


### -field ColorMatrixFlagsSkipGrays

Specifies that colors are adjusted but gray shades are not adjusted. A gray shade is any color that has the same value for its red, green, and blue components. 


### -field ColorMatrixFlagsAltGray

Specifies that colors are adjusted by one matrix and gray shades are adjusted by another matrix. 


## -see-also




<a href="https://msdn.microsoft.com/4f98fe5b-a1fc-417c-ba08-ddcf0648de21">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/2043d592-e79a-45ce-8964-25ed245e4373">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/e0e00985-e422-4775-8ee2-a17d97214a25">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/6fe73738-41f6-4ff3-bcd5-a885040bf48b">ImageAttributes::SetColorMatrix</a>
 

 

