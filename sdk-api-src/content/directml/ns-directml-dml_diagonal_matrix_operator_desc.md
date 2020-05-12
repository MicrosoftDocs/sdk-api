---
UID: NS:directml.DML_DIAGONAL_MATRIX_OPERATOR_DESC
title: DML_DIAGONAL_MATRIX_OPERATOR_DESC
description: Describes a DirectML math operator that generates an identity-like matrix with ones on the major diagonal and zeros everywhere else.
tech.root: direct3d12
ms.date: 01/31/2020
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
 - directml/DML_DIAGONAL_MATRIX_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML math operator that generates an identity-like matrix with ones on the major diagonal and zeros everywhere else. The diagonal ones may be shifted (via *Offset*) where `output[i, i + Offset] = 1`, meaning that arguments of *Offset* greater than zero shifts all ones to the right, and less than zero shifts them to the left.

This generator operator is useful for models. The input is restricted to two dimensions because that's the primary use case.

```
output.shape = input.shape
output.type = if (exists(dtype)) then dtype else input.type
// Any axis greater than H and W are treated as batch counts.
for each coordinate in output tensor
    output[coordinate] = if (coordinate.h + k == coordinate.w) then 1 else 0
endfor

//  Example.
//  k = 0 // default identity matrix
//  input[2, 3] = [...] // Only the shape matters; not the content.
//  output = [[1, 0],
//            [0, 1],
//            [0, 0]]
//  k = -1 // shift ones down
//  input[2, 3] = [...] // Only the shape matters; not the content.
//  output = [[0, 0],
//            [1, 0],
//            [0, 1]]
//  k = -3 // Shift the diagonal line of ones so far as to make all zeroes.
//  input[2, 3] = [...] // Only the shape matters; not the content.
//  output = [[0, 0],
//            [0, 0],
//            [0, 0]]
//  k = 1 // shift ones right
//  input[3, 3] = [...] // Only the shape matters; not the content.
//  output = [[ 0,  1,  0],
//            [ 0,  0,  1],
//            [ 0,  0,  0]]
```

## -struct-fields

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field Offset

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

An offset to shift the ones by.

### -field Value

Type: **[FLOAT](/windows/desktop/winprog/windows-data-types)**

TBD

## -remarks

## -see-also
