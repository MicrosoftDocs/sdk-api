---
UID: NS:directml.DML_LP_NORMALIZATION_OPERATOR_DESC
title: DML_LP_NORMALIZATION_OPERATOR_DESC
description: Performs an Lp-normalization function along the specified axis of the input tensor.
helpviewer_keywords: ["DML_LP_NORMALIZATION_OPERATOR_DESC","DML_LP_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_lp_normalization_operator_desc","directml/DML_LP_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_lp_normalization_operator_desc.htm
tech.root: directml
ms.assetid: EEE59313-F8F4-4617-9499-1BEF5A4C635D
ms.date: 11/02/2020
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
 - DML_LP_NORMALIZATION_OPERATOR_DESC
 - directml/DML_LP_NORMALIZATION_OPERATOR_DESC
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
 - DML_LP_NORMALIZATION_OPERATOR_DESC
---

## -description

Performs an Lp-normalization function along the specified axis of the input tensor.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the input data.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. This tensor's *Sizes* should match the *InputTensor*.

### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis on which to apply normalization.

### -field Epsilon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero. A value of 0.00001 is recommended as default.

### -field P

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The order of the normalization (either 1 or 2).

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints

*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support

### DML_FEATURE_LEVEL_3_1 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_1_0 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
