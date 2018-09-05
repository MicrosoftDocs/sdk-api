---
UID: NE:d2d1effects_1.D2D1_YCBCR_PROP
title: D2D1_YCBCR_PROP
author: windows-sdk-content
description: Identifiers for properties of the YCbCr effect.
old-location: direct2d\d2d1_ycbcr_prop.htm
old-project: direct2d
ms.assetid: 08019B09-0254-48B3-9213-3E7362358109
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_YCBCR_PROP, D2D1_YCBCR_PROP enumeration [Direct2D], D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING, D2D1_YCBCR_PROP_INTERPOLATION_MODE, D2D1_YCBCR_PROP_TRANSFORM_MATRIX, d2d1effects_1/D2D1_YCBCR_PROP, d2d1effects_1/D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING, d2d1effects_1/D2D1_YCBCR_PROP_INTERPOLATION_MODE, d2d1effects_1/D2D1_YCBCR_PROP_TRANSFORM_MATRIX, direct2d.d2d1_ycbcr_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: D2D1_YCBCR_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_1.h
api_name:
 - D2D1_YCBCR_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
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



