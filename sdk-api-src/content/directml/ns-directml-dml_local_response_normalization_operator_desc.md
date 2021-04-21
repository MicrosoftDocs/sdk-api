---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
description: Performs a local response normalization (LRN) function on the input.
helpviewer_keywords: ["DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC","DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_local_response_normalization_operator_desc","directml/DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_local_response_normalization_operator_desc.htm
tech.root: directml
ms.assetid: 43C494DC-4922-4944-A07F-802B43122575
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
 - DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
 - directml/DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
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
 - DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
---

## -description

Performs a local response normalization (LRN) function on the input. This operator performs the following computation.

```
Output = Input / (Bias + (Alpha / LocalSize) * sum(Input^2 for every Input in the local region))^Beta
```

The data type and size of the input and output tensors must be the same.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the input data. This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. This tensor's *Sizes* should match the *InputTensor*.

### -field CrossChannel

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

**TRUE** if the LRN layer sums across channels; otherwise, **FALSE**.

### -field LocalSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of elements to sum over per dimension: Width, Height, and optionally Channel (if *CrossChannel* is set). This value must be at least 1.

### -field Alpha

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scaling parameter. A value of 0.0001 is recommended as default.

### -field Beta

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the exponent. A value of 0.75 is recommended as default.

### -field Bias

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of bias. A value of 1 is recommended as default.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
