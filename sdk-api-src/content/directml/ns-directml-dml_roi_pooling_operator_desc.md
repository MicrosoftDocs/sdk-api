---
UID: NS:directml.DML_ROI_POOLING_OPERATOR_DESC
title: DML_ROI_POOLING_OPERATOR_DESC
description: Performs a MaxPool function across the input tensor (according to regions of interest, or ROIs).
helpviewer_keywords: ["DML_ROI_POOLING_OPERATOR_DESC","DML_ROI_POOLING_OPERATOR_DESC structure","direct3d12.dml_roi_pooling_operator_desc","directml/DML_ROI_POOLING_OPERATOR_DESC"]
old-location: direct3d12\dml_roi_pooling_operator_desc.htm
tech.root: directml
ms.assetid: 7A165306-AC29-4C80-9586-2FB37E85147E
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
 - DML_ROI_POOLING_OPERATOR_DESC
 - directml/DML_ROI_POOLING_OPERATOR_DESC
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
 - DML_ROI_POOLING_OPERATOR_DESC
---

## -description

Performs a MaxPool function across the input tensor (according to regions of interest, or ROIs). For each output element, the coordinates of its corresponding ROI in the input are computed by the following equations.

Let `Y` be an index into the third dimension of *InputTensor* (`{ BatchSize, ChannelCount, **height**, width }`).

Let `X` be an index into the fourth dimension of *InputTensor* (`{ BatchSize, ChannelCount, height, **width** }`).

```
x1 = round(RoiX1 * SpatialScale)
x2 = round(RoiX2 * SpatialScale)
y1 = round(RoiY1 * SpatialScale)
y2 = round(RoiY2 * SpatialScale)

RegionHeight = y2 - y1 + 1
RegionWidth = x2 - x1 + 1

StartY = (OutputIndices.Y * RegionHeight) / PooledSize.Height + y1
StartX = (OutputIndices.X * RegionWidth) / PooledSize.Width + x1

EndY = ((OutputIndices.Y + 1) * RegionHeight + PooledSize.Height - 1) / PooledSize.Height + y1
EndX = ((OutputIndices.X + 1) * RegionWidth + PooledSize.Width - 1) / PooledSize.Width + x1
```

If the computed coordinates are out of bounds, then they are clamped to the input boundaries.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.

### -field ROITensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the regions of interest (ROI) data. The expected dimensions of `ROITensor` are `{ 1, 1, NumROIs, 5 }` and the data for each ROI is `[BatchID, x1, y1, x2, y2]`. x1, y1, x2, y2 are the inclusive coordinates of the corners of each ROI and x2 >= x1, y2 >= y1.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the output data. The expected dimensions of *OutputTensor* are `{ NumROIs, InputChannelCount, PooledSize.Height, PooledSize.Width }`.

### -field SpatialScale

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Multiplicative spatial scale factor used to translate the ROI coordinates from their input scale to the scale used when pooling.

### -field PooledSize

Type: [**DML_SIZE_2D**](/windows/win32/api/directml/ns-directml-dml_size_2d)

The ROI pool output size (height, width), which must match the last 2 dimensions of *OutputTensor*.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ROITensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
