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

# D2D1_2DAFFINETRANSFORM_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/E8973EBE-764C-4220-BB1E-3BFD4853582D">2D affine transform effect</a>.


## -enum-fields




### -field D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE


            The interpolation mode used to scale the image. There are 6 scale modes that range in quality and speed.
            

Type is <a href="https://msdn.microsoft.com/FCD3A8BA-6628-4E81-9488-35A4A1B23DDF">D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE</a>.

Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.


### -field D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard.
            

Type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

Default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX


            The 3x2 matrix to transform the image using the Direct2D matrix transform.
            

Type is <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>.

Default value is Matrix3x2F::Identity().


### -field D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS


            In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1. The values are unitless. You can use sharpness to adjust the quality of an image when you scale the image.
            The sharpness factor affects the shape of the kernel. The higher the sharpness factor, the smaller the kernel.
            

<div class="alert"><b>Note</b>  This property affects only the high quality cubic interpolation mode.</div>
<div> </div>
Type is FLOAT.

Default value is 1.0f.


### -field D2D1_2DAFFINETRANSFORM_PROP_FORCE_DWORD



