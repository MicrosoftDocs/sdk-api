---
UID: NE:gdiplusenums.InterpolationMode
title: InterpolationMode
author: windows-sdk-content
description: The InterpolationMode enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the Graphics::GetInterpolationMode and Graphics::SetInterpolationMode methods of the Graphics class.
old-location: gdiplus\_gdiplus_ENUM_InterpolationMode.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\interpolationmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: InterpolationMode, InterpolationMode enumeration [GDI+], InterpolationModeBicubic, InterpolationModeBilinear, InterpolationModeDefault, InterpolationModeHighQuality, InterpolationModeHighQualityBicubic, InterpolationModeHighQualityBilinear, InterpolationModeInvalid, InterpolationModeLowQuality, InterpolationModeNearestNeighbor, _gdiplus_ENUM_InterpolationMode, gdiplus._gdiplus_ENUM_InterpolationMode, gdiplusenums/InterpolationMode, gdiplusenums/InterpolationModeBicubic, gdiplusenums/InterpolationModeBilinear, gdiplusenums/InterpolationModeDefault, gdiplusenums/InterpolationModeHighQuality, gdiplusenums/InterpolationModeHighQualityBicubic, gdiplusenums/InterpolationModeHighQualityBilinear, gdiplusenums/InterpolationModeInvalid, gdiplusenums/InterpolationModeLowQuality, gdiplusenums/InterpolationModeNearestNeighbor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdiplusenums.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - InterpolationMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# InterpolationMode enumeration


## -description


The <b>InterpolationMode</b> enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the <a href="https://msdn.microsoft.com/a9f3b27c-cb16-4d52-9970-ea3708bd1e0c">Graphics::GetInterpolationMode</a> and <a href="https://msdn.microsoft.com/1624691c-fbf0-4d14-8d48-e7c69e0100aa">Graphics::SetInterpolationMode</a> methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class.


## -enum-fields




### -field InterpolationModeInvalid

Used internally


### -field InterpolationModeDefault

Specifies the default interpolation mode. 


### -field InterpolationModeLowQuality

Specifies a low-quality mode. 


### -field InterpolationModeHighQuality

Specifies a high-quality mode. 


### -field InterpolationModeBilinear

Specifies bilinear interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 50 percent of its original size. 


### -field InterpolationModeBicubic

Specifies bicubic interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 25 percent of its original size. 


### -field InterpolationModeNearestNeighbor

Specifies nearest-neighbor interpolation. 


### -field InterpolationModeHighQualityBilinear

Specifies high-quality, bilinear interpolation. Prefiltering is performed to ensure high-quality shrinking. 


### -field InterpolationModeHighQualityBicubic

Specifies high-quality, bicubic interpolation. Prefiltering is performed to ensure high-quality shrinking. This mode produces the highest quality transformed images. 


## -see-also




<a href="https://msdn.microsoft.com/a9f3b27c-cb16-4d52-9970-ea3708bd1e0c">Graphics::GetInterpolationMode</a>



<a href="https://msdn.microsoft.com/1624691c-fbf0-4d14-8d48-e7c69e0100aa">Graphics::SetInterpolationMode</a>
 

 

