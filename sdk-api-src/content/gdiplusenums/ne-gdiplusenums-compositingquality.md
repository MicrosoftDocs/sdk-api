---
UID: NE:gdiplusenums.CompositingQuality
title: CompositingQuality
author: windows-sdk-content
description: The CompositingQuality enumeration specifies whether gamma correction is applied when colors are blended with background colors.
old-location: gdiplus\_gdiplus_ENUM_CompositingQuality.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\compositingquality.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CompositingQuality, CompositingQuality enumeration [GDI+], CompositingQualityAssumeLinear, CompositingQualityDefault, CompositingQualityGammaCorrected, CompositingQualityHighQuality, CompositingQualityHighSpeed, _gdiplus_ENUM_CompositingQuality, gdiplus._gdiplus_ENUM_CompositingQuality, gdiplusenums/CompositingQuality, gdiplusenums/CompositingQualityAssumeLinear, gdiplusenums/CompositingQualityDefault, gdiplusenums/CompositingQualityGammaCorrected, gdiplusenums/CompositingQualityHighQuality, gdiplusenums/CompositingQualityHighSpeed
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CompositingQuality enumeration


## -description


The <b>CompositingQuality</b> enumeration specifies whether gamma correction is applied when colors are blended with background colors. This enumeration is used by the <a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a> and <a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a> methods of the 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> class.


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




<a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a>
 

 

