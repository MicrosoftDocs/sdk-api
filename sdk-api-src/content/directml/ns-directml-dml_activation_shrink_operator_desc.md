---
UID: NS:directml.DML_ACTIVATION_SHRINK_OPERATOR_DESC
title: DML_ACTIVATION_SHRINK_OPERATOR_DESC
description: Performs the shrink activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.
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
 - DML_ACTIVATION_SHRINK_OPERATOR_DESC
f1_keywords:
 - DML_ACTIVATION_SHRINK_OPERATOR_DESC
 - directml/DML_ACTIVATION_SHRINK_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Performs the shrink activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(x) = x - Bias, if x > Threshold
       x + Bias, if x < -Threshold
       0,        otherwise
```

This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

The output tensor to write the results to.

### -field Bias

Type: **[FLOAT](/windows/desktop/WinProg/windows-data-types)**

The value of the bias. A typical default for this value is 0.0.

### -field Threshold

Type: **[FLOAT](/windows/desktop/WinProg/windows-data-types)**

The value of the threshold. A typical default for this value is 0.5.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_5_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |

## -see-also
