---
UID: NS:directml.DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
description: Describes a DirectML math operator that determines, elementwise, whether the input is NaN.
tech.root: directml
ms.date: 01/30/2020
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
 - DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML math operator that determines, elementwise, whether the input is NaN.

```
For each x in InputTensor
    // Can test float32 IEEE 754 NaN by looking for an 8-bit exponent set to all ones
    // and any bit of the 23-bit mantissa set (sign-ignorable).
    IsNan(x) = (asuint(x) & 0x7FFFFFFF) > 0x7F800000
```

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

## -remarks

## -see-also

