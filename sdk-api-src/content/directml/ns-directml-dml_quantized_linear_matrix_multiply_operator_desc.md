---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Performs a matrix multiplication function on quantized data. This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.
helpviewer_keywords: ["DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC","DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure","direct3d12.dml_quantized_linear_matrix_multiply_operator_desc","directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC"]
tech.root: directml
ms.date: 08/21/2024
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
f1_keywords:
 - DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
 - directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
 - DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
---

## -description

Performs a matrix multiplication function on quantized data. This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.

This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`. The matrix multiply operator will perform BatchCount * ChannelCount number of independent matrix multiplications. 

For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount * ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}. 

### Dequantize function

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### Quantize function

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the A data. This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.

### -field AScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the ATensor scale data. The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required. These scale values are used for dequantizing the A values.

> [!NOTE]
> A scale value of 0 results in undefined behavior.

### -field AZeroPointTensor

Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the *ATensor* zero point data. The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required. These zero point values are used for dequantizing the ATensor values.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the B data. This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.

### -field BScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the *BTensor* scale data. The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required. These scale values are used for dequantizing the *BTensor* values.

> [!NOTE]
> A scale value of 0 results in undefined behavior.

### -field BZeroPointTensor

Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the *BTensor* zero point data. The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required. These zero point values are used for dequantizing the *BTensor* values.

### -field OutputScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the *OutputTensor* scale data. The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per-tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required. This scale value is used for dequantizing the *OutputTensor* values.

> [!NOTE]
> A scale value of 0 results in undefined behavior.

### -field OutputZeroPointTensor

Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the *OutputTensor* zero point data. The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per-tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required. This zero point value is used for dequantizing the *OutputTensor* values.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to. This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_1`.

## Tensor constraints
* *AScaleTensor*, *AZeroPointTensor*, *BScaleTensor*, *BZeroPointTensor*, *OutputScaleTensor*, and *OutputZeroPointTensor* must have the same *DimensionCount*.
* *ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount*.
* *BTensor* and *BZeroPointTensor* must have the same *DataType*.
* *OutputTensor* and *OutputZeroPointTensor* must have the same *DataType*.
* *AScaleTensor*, *AZeroPointTensor*, *BScaleTensor*, *BZeroPointTensor*, *OutputScaleTensor*, and *OutputZeroPointTensor* must have the same *DimensionCount*.
* *ATensor* and *AZeroPointTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_4_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 2 to 4 | INT8, UINT8 |
| AScaleTensor | Input | 1 to 4 | FLOAT32 |
| AZeroPointTensor | Optional input | 1 to 4 | INT8, UINT8 |
| BTensor | Input | 2 to 4 | INT8, UINT8 |
| BScaleTensor | Input | 1 to 4 | FLOAT32 |
| BZeroPointTensor | Optional input | 1 to 4 | INT8, UINT8 |
| OutputScaleTensor | Input | 1 to 4 | FLOAT32 |
| OutputZeroPointTensor | Optional input | 1 to 4 | INT8, UINT8 |
| OutputTensor | Output | 2 to 4 | INT8, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 | INT8, UINT8 |
| AScaleTensor | Input | 4 | FLOAT32 |
| AZeroPointTensor | Optional input | 4 | INT8, UINT8 |
| BTensor | Input | 4 | INT8, UINT8 |
| BScaleTensor | Input | 4 | FLOAT32 |
| BZeroPointTensor | Optional input | 4 | INT8, UINT8 |
| OutputScaleTensor | Input | 4 | FLOAT32 |
| OutputZeroPointTensor | Optional input | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |
