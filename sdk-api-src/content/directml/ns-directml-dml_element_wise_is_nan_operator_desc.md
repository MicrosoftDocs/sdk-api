---
UID: NS:directml.DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC
description: For each element of the input tensor, returns 1 if the input is NaN (as defined by IEEE-754), and 0 otherwise. The result is placed into the corresponding element of the output tensor.
tech.root: directml
ms.date: 10/29/2020
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

For each element of the input tensor, returns 1 if the input is NaN (as defined by IEEE-754), and 0 otherwise. The result is placed into the corresponding element of the output tensor.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | UINT32, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | UINT32, UINT8 |

## -see-also
