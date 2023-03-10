---
UID: NS:directml.DML_DIAGONAL_MATRIX_OPERATOR_DESC
title: DML_DIAGONAL_MATRIX_OPERATOR_DESC
description: Generates an identity-like matrix with ones (or other explicit value) on the major diagonal, and zeros everywhere else.
tech.root: directml
ms.date: 07/20/2022
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
 - DML_DIAGONAL_MATRIX_OPERATOR_DESC
f1_keywords:
 - DML_DIAGONAL_MATRIX_OPERATOR_DESC
 - directml/DML_DIAGONAL_MATRIX_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Generates an identity-like matrix with ones (or other explicit value) on the major diagonal, and zeros everywhere else. The diagonal ones may be shifted (via *Offset*) where `OutputTensor[i, i + Offset]` = *Value*, meaning that an argument of *Offset* greater than zero shifts all values to the right, and less than zero shifts them to the left. This generator operator is useful for models to avoid storing a large constant tensor. Any leading dimensions before the last two are treated as a batch count, meaning that the tensor is treated as stack of 2D matrices.

This operator performs the following pseudocode.

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = if (coordinate.y + Offset == coordinate.x) then Value else 0
endfor
```

## -struct-fields

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. The dimensions are `{ Batch1, Batch2, OutputHeight, OutputWidth }`. The height and width don't need to be square.

### -field Offset

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

An offset to shift the diagonal lines of *Value*, with positive offsets shifting the written value to the right/up (viewing the output as a matrix with the top left as 0,0), and negative offsets to the left/down.

### -field Value

Type: **[FLOAT](/windows/desktop/winprog/windows-data-types)**

A value to fill along the 2D diagonal. The standard value is 1.0. Note that if the *DataType* of the tensors is not [DML_TENSOR_DATA_TYPE_FLOAT16](/windows/win32/api/directml/ne-directml-dml_tensor_data_type) or **DML_TENSOR_DATA_TYPE_FLOAT32**, then the value might be truncated (for example, 10.6 will become 10).

## Examples

Default identity matrix:

```
Offset: 0
Value: 1.0
OutputTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
    [[[[1, 0, 0],
       [0, 1, 0],
       [0, 0, 1]]]]
```

Shift ones right/up:

```
Offset: 1
Value: 1.0
OutputTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
    [[[[ 0, 1, 0],
       [ 0, 0, 1],
       [ 0, 0, 0]]]]
```

Shift ones left/down:

```
Offset: -1
Value: 1.0
OutputTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
    [[[[0, 0],
       [1, 0],
       [0, 1]]]]
```

Shift the diagonal line of ones so far that all become zeroes:

```
Offset: -3
Value: 1.0
OutputTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
    [[[[0, 0],
       [0, 0],
       [0, 0]]]]
```

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor support
### DML_FEATURE_LEVEL_5_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Output | 2 to 4 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_4_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Output | 2 to 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also
