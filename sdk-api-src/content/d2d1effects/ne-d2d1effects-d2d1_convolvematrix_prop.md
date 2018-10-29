---
UID: NE:d2d1effects.D2D1_CONVOLVEMATRIX_PROP
title: D2D1_CONVOLVEMATRIX_PROP
author: windows-sdk-content
description: Identifiers for properties of the Convolve matrix effect.
old-location: direct2d\d2d1_convolvematrix_prop.htm
tech.root: Direct2D
ms.assetid: B6ACCA00-8127-4F4B-BF3B-9789943C0BB1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: D2D1_CONVOLVEMATRIX_PROP, D2D1_CONVOLVEMATRIX_PROP enumeration [Direct2D], D2D1_CONVOLVEMATRIX_PROP_BIAS, D2D1_CONVOLVEMATRIX_PROP_BORDER_MODE, D2D1_CONVOLVEMATRIX_PROP_CLAMP_OUTPUT, D2D1_CONVOLVEMATRIX_PROP_DIVISOR, D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, D2D1_CONVOLVEMATRIX_PROP_KERNEL_OFFSET, D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_X, D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_Y, D2D1_CONVOLVEMATRIX_PROP_KERNEL_UNIT_LENGTH, D2D1_CONVOLVEMATRIX_PROP_PRESERVE_ALPHA, D2D1_CONVOLVEMATRIX_PROP_SCALE_MODE, d2d1effects/D2D1_CONVOLVEMATRIX_PROP, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_BIAS, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_BORDER_MODE, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_DIVISOR, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_KERNEL_OFFSET, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_X, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_Y, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_PRESERVE_ALPHA, d2d1effects/D2D1_CONVOLVEMATRIX_PROP_SCALE_MODE, direct2d.d2d1_convolvematrix_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_CONVOLVEMATRIX_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_CONVOLVEMATRIX_PROP
req.redist: 
---

# D2D1_CONVOLVEMATRIX_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/D9C23AC4-0090-4F16-AC59-B952FB616FA9">Convolve matrix effect</a>.


## -enum-fields




### -field D2D1_CONVOLVEMATRIX_PROP_KERNEL_UNIT_LENGTH

The size of one unit in the kernel. The units are in (DIPs/kernel unit), where a kernel unit is the size of the element in the convolution kernel. 
          A value of 1 (DIP/kernel unit) corresponds to one pixel in a image at 96 DPI.
          

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_CONVOLVEMATRIX_PROP_SCALE_MODE

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
          

The type is <a href="https://msdn.microsoft.com/16949437-83A6-41D2-B531-089ACE748E3F">D2D1_CONVOLVEMATRIX_SCALE_MODE</a>.

The default value is D2D1_CONVOLVEMATRIX_SCALE_MODE_LINEAR.


### -field D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_X

The width of the kernel matrix. The units are specified in kernel units. 
          

The type is UINT32.

The default value is 3.


### -field D2D1_CONVOLVEMATRIX_PROP_KERNEL_SIZE_Y

The height of the kernel matrix. The units are specified in kernel units. 
          

The type is UINT32.

The default value is 3.


### -field D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX

The kernel matrix to be applied to the image. The kernel elements aren't bounded and are specified as floats.
          

The first set of KernelSizeX numbers in the FLOAT[] corresponds to the first row in the kernel.
          The second set of KernelSizeX numbers correspond to the second row, and so on up to KernelSizeY rows.

The type is FLOAT[].

The default value is {0.0f, 0.0f, 0.0f, 0.0f, 1.0f, 0.0f, 0.0f, 0.0f, 0.0f}.


### -field D2D1_CONVOLVEMATRIX_PROP_DIVISOR

The kernel matrix is applied to a pixel and then the result is divided by this value. 
          

0 behaves as a value of float epsilon.

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_CONVOLVEMATRIX_PROP_BIAS

The effect applies the kernel matrix, the divisor, and then the bias is added to the result. The bias is unbounded and unitless. 
          

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_CONVOLVEMATRIX_PROP_KERNEL_OFFSET

Shifts the convolution kernel from a centered position on the output pixel to a position you specify left/right and up/down. The offset is defined in kernel units.
          

With some offsets and kernel sizes, the convolution kernel’s samples won't land on a pixel image center. The pixel values for the kernel sample are computed by bilinear interpolation.

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is {0.0f, 0.0f}.


### -field D2D1_CONVOLVEMATRIX_PROP_PRESERVE_ALPHA

Specifies whether the convolution kernel is applied to the alpha channel or only the color channels.
          

If you set this to TRUE the convolution kernel is applied only to the color channels.

If you set this to FALSE the convolution kernel is applied to all channels.

The type is BOOL.

The default value is FALSE.


### -field D2D1_CONVOLVEMATRIX_PROP_BORDER_MODE

The mode used to calculate the border of the image, soft or hard.
          

The type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_CONVOLVEMATRIX_PROP_CLAMP_OUTPUT

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. The effect clamps the values before it premultiplies the alpha.
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
          but other effects and the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default value is FALSE.


### -field D2D1_CONVOLVEMATRIX_PROP_FORCE_DWORD



