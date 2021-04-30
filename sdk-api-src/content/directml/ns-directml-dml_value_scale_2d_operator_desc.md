---
UID: NS:directml.DML_VALUE_SCALE_2D_OPERATOR_DESC
title: DML_VALUE_SCALE_2D_OPERATOR_DESC
description: Performs an element-wise scale-and-bias function, `Output = Scale * Input + Bias`.
helpviewer_keywords: ["DML_VALUE_SCALE_2D_OPERATOR_DESC","DML_VALUE_SCALE_2D_OPERATOR_DESC structure","direct3d12.dml_value_scale_2d_operator_desc","directml/DML_VALUE_SCALE_2D_OPERATOR_DESC"]
old-location: direct3d12\dml_value_scale_2d_operator_desc.htm
tech.root: directml
ms.assetid: 205124C7-9296-4D13-9EC9-55B03D4E0595
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
 - DML_VALUE_SCALE_2D_OPERATOR_DESC
 - directml/DML_VALUE_SCALE_2D_OPERATOR_DESC
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
 - DML_VALUE_SCALE_2D_OPERATOR_DESC
---

## -description

Performs an element-wise scale-and-bias function, `Output = Scale * Input + Bias`. This operator is similar to using an [DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_identity_operator_desc) with a scale and bias, except that **DML_VALUE_SCALE_2D_OPERATOR_DESC** applies a different bias for each channel, rather than a single bias for the entire tensor.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Input data. This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor with which to write the results to. This tensor's dimensions should match the *InputTensor*'s dimensions.

### -field Scale

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Scale value to be applied to all input values.

### -field ChannelCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the Bias array. This field must be set to either 1 or 3, and must also match the size of the Channel dimension of the input tensor.

### -field Bias

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a>*</b>

An array of *FLOAT* values containing the bias term for each dimension of the input tensor.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
