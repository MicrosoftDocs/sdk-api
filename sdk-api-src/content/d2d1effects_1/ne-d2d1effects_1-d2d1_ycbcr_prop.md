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

# D2D1_YCBCR_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/E4492996-54DA-4C5F-B44C-8FBE97C8DD7D">YCbCr effect</a>.
        


## -enum-fields




### -field D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING


            Specifies the chroma subsampling of the input chroma image.
            

The type is <a href="https://msdn.microsoft.com/4B0BDC1D-B39C-4787-90D3-50845C3A2B9A">D2D1_YCBCR_CHROMA_SUBSAMPLING</a>.

The default value is D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO.


### -field D2D1_YCBCR_PROP_TRANSFORM_MATRIX


            A 3x2 Matrix specifying the axis-aligned affine transform of the image. Axis aligned transforms include Scale, Flips, and 90 degree rotations.
            

The type is <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>.

The default value is Matrix3x2F::Identity().


### -field D2D1_YCBCR_PROP_INTERPOLATION_MODE


            The interpolation mode.
            

The type is <a href="https://msdn.microsoft.com/30F27963-DF93-46B6-A30E-F89AD634C987">D2D1_YCBCR_INTERPOLATION_MODE</a>.


### -field D2D1_YCBCR_PROP_FORCE_DWORD



