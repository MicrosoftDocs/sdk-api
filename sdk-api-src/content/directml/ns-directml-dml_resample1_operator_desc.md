---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size. You can use a linear or nearest-neighbor interpolation mode.
tech.root: directml
ms.date: 07/20/2022
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
 - DML_RESAMPLE1_OPERATOR_DESC
 - directml/DML_RESAMPLE1_OPERATOR_DESC
---

## -description

Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size. You can use a linear or nearest-neighbor interpolation mode. The operator supports interpolation across multiple dimensions, not just 2D. So you can keep the same spatial size, but interpolate across channels or across batches. The relationship between the input and output coordinates is the following.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the input data.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the output data to.

### -field InterpolationMode

Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

This field determines the kind of interpolation used to choose output pixels.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.

- **DML_INTERPOLATION_MODE_LINEAR**. Uses the *Linear Interpolation* algorithm, which computes the output element by computing the weighted average of the 2 nearest neighboring input elements per dimension. Resampling is supported up to 4 dimensions (quadrilinear), where the weighted average is computed on a total of 16 input elements for each output element.

### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to. This value must match the dimension count of *InputTensor* and *OutputTensor*.

### -field Scales

Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***

The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension. Note that the scales don't need to be exactly `OutputSize / InputSize`. If the input after scaling is larger than the output bound, then we crop it to the output size. On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.

### -field InputPixelOffsets

Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***

The offsets to apply to the input pixels before resampling. When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result. To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.

### -field OutputPixelOffsets

Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***

The offsets to apply to the output pixels after resampling. When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result. To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.

## -remarks
When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_1`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support
### DML_FEATURE_LEVEL_5_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 4 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
