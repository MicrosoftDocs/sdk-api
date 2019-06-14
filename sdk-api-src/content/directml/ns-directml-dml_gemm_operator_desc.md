---
UID: NS:directml.DML_GEMM_OPERATOR_DESC
title: DML_GEMM_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML operator that performs a general matrix multiplication function on the input, y = alpha * transposeA(A) * transposeB(B) + beta * C .
old-location: direct3d12\dml_gemm_operator_desc.htm
tech.root: direct3d12
ms.assetid: 11482420-678E-4914-90F0-9F952BC09FF7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_GEMM_OPERATOR_DESC, DML_GEMM_OPERATOR_DESC structure, direct3d12.dml_gemm_operator_desc, directml/DML_GEMM_OPERATOR_DESC
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_GEMM_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_GEMM_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a general matrix multiplication function on the input, y = alpha * transposeA(A) * transposeB(B) + beta * C
.


## -struct-fields




### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>A</i> tensor to read from. This tensor's dimensions should be [M, K] if <i>TransA</i> is [DML_MATRIX_TRANSFORM_NONE](/windows/desktop/api/directml/ne-directml-dml_matrix_transform), or [K, M] if <i>TransA</i> is <b>DML_MATRIX_TRANSFORM_TRANSPOSE</b>.


### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>B</i> tensor to read from. This tensor's dimensions should be [K, N] if <i>TransB</i> is [DML_MATRIX_TRANSFORM_NONE](/windows/desktop/api/directml/ne-directml-dml_matrix_transform), or [N, K] if <i>TransB</i> is <b>DML_MATRIX_TRANSFORM_TRANSPOSE</b>.


### -field CTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>C</i> tensor to read from, or `nullptr`. This tensor's dimensions should be unidirectional broadcastable to [M, N].


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to. This tensor's dimensions are [M, N].


### -field TransA

Type: [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform)

The transform to be applied to <i>ATensor</i>; either a transpose, or no transform.


### -field TransB

Type: [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform)

The transform to be applied to <i>BTensor</i>; either a transpose, or no transform.


### -field Alpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scalar multiplier for the product of inputs <i>ATensor</i> and <i>BTensor</i>.


### -field Beta

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scalar multiplier for the optional input <i>CTensor</i>.


### -field FusedActivation

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

An optional pointer to a constant [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the fused activation layer.

