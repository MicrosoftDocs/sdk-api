---
UID: NS:directml.DML_UPSAMPLE_2D_OPERATOR_DESC
title: DML_UPSAMPLE_2D_OPERATOR_DESC
description: Upsamples the input image, writing the result into the output tensor. The order of the dimensions should be NCHW (BatchSize, ChannelCount, Height, Width) or NCDHW (BatchSize, ChannelCount, Depth, Height, Width), but strides can be used if the data is stored in a different format.
helpviewer_keywords: ["DML_UPSAMPLE_2D_OPERATOR_DESC","DML_UPSAMPLE_2D_OPERATOR_DESC structure","direct3d12.dml_upsample_2d_operator_desc","directml/DML_UPSAMPLE_2D_OPERATOR_DESC"]
old-location: direct3d12\dml_upsample_2d_operator_desc.htm
tech.root: directml
ms.assetid: 45CA3670-DD38-4617-BF97-CC4133A9FD6D
ms.date: 11/04/2020
req.header: directml.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_UPSAMPLE_2D_OPERATOR_DESC
 - directml/DML_UPSAMPLE_2D_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_UPSAMPLE_2D_OPERATOR_DESC
---

## -description

Upsamples the input image, writing the result into the output tensor. The order of the dimensions should be NCHW (BatchSize, ChannelCount, Height, Width) or NCDHW (BatchSize, ChannelCount, Depth, Height, Width), but strides can be used if the data is stored in a different format. Unlike [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), only the last 2 dimensions (height and width) can be upsampled.

If available, you should prefer [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc) since it is a more flexible version of **DML_UPSAMPLE_2D_OPERATOR_DESC**.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data. The expected dimensions of the InputTensor are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` for 4D, and `{ InputBatchCount, InputChannelCount, InputDepth, InputHeight, InputWidth }` for 5D.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data. The expected dimensions of the OutputTensor are `{ InputBatchCount, InputChannelCount, InputHeight * HeightScale, InputWidth * WidthScale }` for 4D, and `{ InputBatchCount, InputChannelCount, InputDepth, InputHeight * HeightScale, InputWidth * WidthScale }` for 5D.

### -field ScaleSize

Type: [**DML_SIZE_2D**](/windows/win32/api/directml/ns-directml-dml_size_2d)

The width and height scales of type UINT to apply when upsampling the input. `0 < ScaleSize.Height <= UINT_MAX / InputHeight` and `0 < ScaleSize.Width <= UINT_MAX / InputWidth`.

### -field InterpolationMode

Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

This field determines the kind of interpolation used to choose output pixels.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.
- **DML_INTERPOLATION_MODE_LINEAR**. Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements in the height dimension, and the 2 nearest neighboring input elements in the width dimension, for a total of 4 elements. This is true even if the input/output DimensionCount is 5. That is, samples are only ever averaged along the width and height dimensions, and never along the batch, channel, or depth.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |
