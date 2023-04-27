---
UID: NS:directml.DML_MAX_UNPOOLING_OPERATOR_DESC
title: DML_MAX_UNPOOLING_OPERATOR_DESC
description: Inverts a max-pooling operation (see [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) for details) by filling the output tensor *OutputTensor* with the values in the input tensor *InputTensor*, as obtained from a max-pooling operation, according to the index values provided in the *IndicesTensor*. The elements in the output tensor untouched by this process are left with zero values.
tech.root: directml
ms.date: 01/19/2022
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - DML_MAX_UNPOOLING_OPERATOR_DESC
f1_keywords:
 - DML_MAX_UNPOOLING_OPERATOR_DESC
 - directml/DML_MAX_UNPOOLING_OPERATOR_DESC
---

## -description

Inverts a max-pooling operation (see [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) for details) by filling the output tensor *OutputTensor* with the values in the input tensor *InputTensor*, as obtained from a max-pooling operation, according to the index values provided in the *IndicesTensor*. The elements in the output tensor untouched by this process are left with zero values.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An input tensor of *Sizes* `{ Batch, Channel, Height, Width }`. The tensor values are obtained from the values in the *OutputTensor* of a max-pooling operation.

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor of indices to the output tensor *OutputTensor* for the values given in the input tensor *InputTensor*. These index values are zero-based, and treat the output tensor as a contiguous one-dimensional array. Both the *InputTensor* and *IndicesTensor* have the same tensor sizes. The tensor values are obtained from the *OutputIndicesTensor* of a max-pooling operation.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An output tensor of the same number of dimensions as the input tensor.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_3_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 4 | UINT64, UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| IndicesTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
