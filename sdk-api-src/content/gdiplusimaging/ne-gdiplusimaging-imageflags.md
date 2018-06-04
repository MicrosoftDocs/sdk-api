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

# ImageFlags enumeration


## -description


The <b>ImageFlags</b> enumeration specifies the attributes of the pixel data contained in an 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. The 
			<a href="https://msdn.microsoft.com/4a519863-9a4a-41c5-891e-4d7747ca0c07">Image::GetFlags</a> method returns an element of this enumeration.


## -enum-fields




### -field ImageFlagsNone

Specifies no format information. 


### -field ImageFlagsScalable

Specifies that the image can be scaled. 


### -field ImageFlagsHasAlpha

Specifies that the pixel data contains alpha values. 


### -field ImageFlagsHasTranslucent

Specifies that the pixel data has alpha values other than 0 (transparent) and 255 (opaque). 


### -field ImageFlagsPartiallyScalable

Specifies that the pixel data is partially scalable with some limitations. 


### -field ImageFlagsColorSpaceRGB

Specifies that the image is stored using an RGB color space. 


### -field ImageFlagsColorSpaceCMYK

Specifies that the image is stored using a CMYK color space. 


### -field ImageFlagsColorSpaceGRAY

Specifies that the image is a grayscale image. 


### -field ImageFlagsColorSpaceYCBCR

Specifies that the image is stored using a YCBCR color space. 


### -field ImageFlagsColorSpaceYCCK

Specifies that the image is stored using a YCCK color space. 


### -field ImageFlagsHasRealDPI

Specifies that dots per inch information is stored in the image. 


### -field ImageFlagsHasRealPixelSize

Specifies that the pixel size is stored in the image. 


### -field ImageFlagsReadOnly

Specifies that the pixel data is read-only. 


### -field ImageFlagsCaching

Specifies that the pixel data can be cached for faster access. 


## -see-also




<a href="https://msdn.microsoft.com/4a519863-9a4a-41c5-891e-4d7747ca0c07">Image::GetFlags</a>
 

 

