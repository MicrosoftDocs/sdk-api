---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CompositingQuality enumeration


## -description


The <b>CompositingQuality</b> enumeration specifies whether gamma correction is applied when colors are blended with background colors. This enumeration is used by the <a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a> and <a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a> methods of the 
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




<a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a>
 

 

