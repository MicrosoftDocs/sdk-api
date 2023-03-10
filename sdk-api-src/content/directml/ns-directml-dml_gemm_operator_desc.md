---
UID: NS:directml.DML_GEMM_OPERATOR_DESC
title: DML_GEMM_OPERATOR_DESC
description: Performs a general matrix multiplication function of the form `Output = FusedActivation(Alpha * TransA(A) x TransB(B) + Beta * C)`, where `x` denotes matrix multiplication, and `*` denotes multiplication with a scalar.
helpviewer_keywords: ["DML_GEMM_OPERATOR_DESC","DML_GEMM_OPERATOR_DESC structure","direct3d12.dml_gemm_operator_desc","directml/DML_GEMM_OPERATOR_DESC"]
old-location: direct3d12\dml_gemm_operator_desc.htm
tech.root: directml
ms.assetid: 11482420-678E-4914-90F0-9F952BC09FF7
ms.date: 12/01/2022
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
 - DML_GEMM_OPERATOR_DESC
 - directml/DML_GEMM_OPERATOR_DESC
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
 - DML_GEMM_OPERATOR_DESC
---

## -description

Performs a general matrix multiplication function of the form `Output = FusedActivation(Alpha * TransA(A) x TransB(B) + Beta * C)`, where `x` denotes matrix multiplication, and `*` denotes multiplication with a scalar.

This operator requires 4D tensors with layout `{ BatchCount, ChannelCount, Height, Width }`, and it will perform BatchCount * ChannelCount number of independent matrix multiplications. 

For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then this operator performs BatchCount * ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}. 

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the A matrix. This tensor's *Sizes* should be `{ BatchCount, ChannelCount, M, K }` if *TransA* is [DML_MATRIX_TRANSFORM_NONE](/windows/win32/api/directml/ne-directml-dml_matrix_transform), or `{ BatchCount, ChannelCount, K, M }` if *TransA* is **DML_MATRIX_TRANSFORM_TRANSPOSE**.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the B matrix. This tensor's *Sizes* should be `{ BatchCount, ChannelCount, K, N }` if *TransB* is [DML_MATRIX_TRANSFORM_NONE](/windows/win32/api/directml/ne-directml-dml_matrix_transform), or `{ BatchCount, ChannelCount, N, K }` if *TransB* is **DML_MATRIX_TRANSFORM_TRANSPOSE**.

### -field CTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the C matrix, or `nullptr`. Values default to 0 when not provided. If provided, this tensor's *Sizes* should be `{ BatchCount, ChannelCount, M, N }`.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. This tensor's *Sizes* are `{ BatchCount, ChannelCount, M, N }`.

### -field TransA

Type: [**DML_MATRIX_TRANSFORM**](/windows/win32/api/directml/ne-directml-dml_matrix_transform)

The transform to be applied to *ATensor*; either a transpose, or no transform.

### -field TransB

Type: [**DML_MATRIX_TRANSFORM**](/windows/win32/api/directml/ne-directml-dml_matrix_transform)

The transform to be applied to *BTensor*; either a transpose, or no transform.

### -field Alpha

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scalar multiplier for the product of inputs *ATensor* and *BTensor*.

### -field Beta

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scalar multiplier for the optional input *CTensor*. If *CTensor* is not provided, then this value is ignored.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the GEMM. For more info, see [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations).

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *ATensor*, *BTensor*, *CTensor*, and *OutputTensor* must have the same *DataType* and *DimensionCount*.
* *CTensor* and *OutputTensor* must have the same *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_4_0 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Input | { [BatchCount], [ChannelCount], M, K } | 2 to 4 | FLOAT32, FLOAT16 |
| BTensor | Input | { [BatchCount], [ChannelCount], K, N } | 2 to 4 | FLOAT32, FLOAT16 |
| CTensor | Optional input | { [BatchCount], [ChannelCount], M, N } | 2 to 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { [BatchCount], [ChannelCount], M, N } | 2 to 4 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Input | { BatchCount, ChannelCount, M, K } | 4 | FLOAT32, FLOAT16 |
| BTensor | Input | { BatchCount, ChannelCount, K, N } | 4 | FLOAT32, FLOAT16 |
| CTensor | Optional input | { BatchCount, ChannelCount, M, N } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { BatchCount, ChannelCount, M, N } | 4 | FLOAT32, FLOAT16 |

## -see-also

* [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
