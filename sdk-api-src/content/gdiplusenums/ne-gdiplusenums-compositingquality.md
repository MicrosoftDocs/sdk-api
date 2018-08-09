---
UID: NE:gdiplusenums.CompositingQuality
title: CompositingQuality
author: windows-sdk-content
description: The CompositingQuality enumeration specifies whether gamma correction is applied when colors are blended with background colors.
old-location: gdiplus\_gdiplus_ENUM_CompositingQuality.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\compositingquality.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CompositingQuality, CompositingQuality enumeration [GDI+], CompositingQualityAssumeLinear, CompositingQualityDefault, CompositingQualityGammaCorrected, CompositingQualityHighQuality, CompositingQualityHighSpeed, _gdiplus_ENUM_CompositingQuality, gdiplus._gdiplus_ENUM_CompositingQuality, gdiplusenums/CompositingQuality, gdiplusenums/CompositingQualityAssumeLinear, gdiplusenums/CompositingQualityDefault, gdiplusenums/CompositingQualityGammaCorrected, gdiplusenums/CompositingQualityHighQuality, gdiplusenums/CompositingQualityHighSpeed
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
 - CompositingQuality
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# CompositingQuality enumeration


## -description


The <b>CompositingQuality</b> enumeration specifies whether gamma correction is applied when colors are blended with background colors. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/ms535701(v=VS.85).aspx">Graphics::GetCompositingQuality</a> and <a href="https://msdn.microsoft.com/en-us/library/ms535809(v=VS.85).aspx">Graphics::SetCompositingQuality</a> methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class.


## -enum-fields




### -field CompositingQualityInvalid


### -field CompositingQualityDefault

Specifies that gamma correction is not applied. 


### -field CompositingQualityHighSpeed

Specifies that gamma correction is not applied. 


### -field CompositingQualityHighQuality

Specifies that gamma correction is applied. 


### -field CompositingQualityGammaCorrected

Specifies that gamma correction is applied. 


### -field CompositingQualityAssumeLinear

Specifies that gamma correction is not applied. 


## -remarks



When you specify that gamma correction should not be applied, the image data to be rendered (blended with the background) is assumed to be in a linear color space with a gamma value of 1.0. As a result, no gamma adjustment is applied to the image data before or after blending the image with the background.

When you specify that gamma correction should be applied, the image data to be rendered (blended with the background) is assumed to be in the sRGB color space with a gamma value of 2.2. To ensure accurate blending, the input image data is transformed into a linear (gamma = 1.0) space before the colors are blended and transformed back into sRGB (gamma = 2.2) space afterward. This mode results in a more accurate blend at the expense of additional processing time. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535701(v=VS.85).aspx">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535809(v=VS.85).aspx">Graphics::SetCompositingQuality</a>
 

 

