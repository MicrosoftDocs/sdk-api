---
UID: NS:directml.DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
title: DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
description: Adds every element in *ATensor* to its corresponding element in *BTensor* and places the result into the corresponding element of *OutputTensor*, with the option for fused activation.
tech.root: directml
ms.date: 12/01/2022
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
 - DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Adds every element in *ATensor* to its corresponding element in *BTensor* and places the result into the corresponding element of *OutputTensor*, with the option for fused activation.

```
f(a, b) = FusedActivation(a + b)
```

The fused activation operator description, if provided, then executes the given activation operator on the output. 

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one or more of the input tensors during binding.

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the left-hand side inputs.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the right-hand side inputs.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the addition. For more info, see [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations).

Fused activation may be used only when the output datatype is **FLOAT16** or **FLOAT32**.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor constraints
*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| BTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| BTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |

## -see-also

* [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
