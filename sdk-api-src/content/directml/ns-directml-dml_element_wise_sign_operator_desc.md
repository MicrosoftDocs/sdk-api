---
UID: NS:directml.DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
title: DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
description: Describes a DirectML operator that performs an elementwise shrink activation function on the input.
tech.root: direct3d12
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
 - DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
f1_keywords:
 - directml/DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML operator that, elementwise, returns the sign of the input.

```
For each x in InputTensor
    if (x > 0) then 1
    else if (x < 0) then -1
    else if (x == 0) then 0
    else NaN
```

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

## -remarks

## -see-also
