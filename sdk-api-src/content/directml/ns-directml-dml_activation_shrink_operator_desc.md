---
UID: NS:directml.DML_ACTIVATION_SHRINK_OPERATOR_DESC
title: DML_ACTIVATION_SHRINK_OPERATOR_DESC
description: Describes a DirectML operator that performs an elementwise shrink activation function on the input.
tech.root: directml
ms.date: 01/24/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directml.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_ACTIVATION_SHRINK_OPERATOR_DESC
f1_keywords:
 - DML_ACTIVATION_SHRINK_OPERATOR_DESC
 - directml/DML_ACTIVATION_SHRINK_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML operator that performs an elementwise shrink activation function on the input.

```
For each x in InputTensor
    if (x < -threshold)
        x = x + bias
    else if (x > threshold)
        x = x - bias
    else x = 0
```

Shrink has no relation to slice, nor resize, despite the naming similarity. It actually 'shrinks' per-element values. And it doesn't always shrink; but can instead grow, depending on the bias sign.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

A pointer to a constant [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

A pointer to a constant [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md) containing the description of the tensor to write the results to.

### -field Bias

Type: **[FLOAT](/windows/desktop/WinProg/windows-data-types)**

The value of bias. You can use a default value of 1.0.

### -field Threshold

Type: **[FLOAT](/windows/desktop/WinProg/windows-data-types)**

The value of threshold.

## -remarks

## -see-also