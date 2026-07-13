---
UID: NF:directxmath.XMFLOAT3X4.XMFLOAT3X4(constfloat)
title: XMFLOAT3X4::XMFLOAT3X4(constfloat)
ms.date: 04/22/2020
description: Constructs an **XMFLOAT3X4** from a 12-element array of float values.
tech.root: dxmath
req.construct-type: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - XMFLOAT3X4::XMFLOAT3X4
 - directxmath/XMFLOAT3X4::XMFLOAT3X4
dev_langs:
 - c++
topic_type:
 - apiref
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmath.h
api_name:
 - XMFLOAT3X4::XMFLOAT3X4
---

## -description

Constructs an **XMFLOAT3X4** from a 12-element array of float values.

## -parameters

### -param pArray

Type: **const float \***

A pointer to a 12-element array of float values. The array specifies the value of each member of the new matrix.

## -remarks

The matrix elements in *pArray* should be in row-major order. These two pseudocode examples illustrate how this constructor operates.

```cpp
DirectX::XMFLOAT3X4 mat;
mat._11 = pArray[0];
mat._12 = pArray[1];
mat._13 = pArray[2];
mat._14 = pArray[3];
mat._21 = pArray[4];
mat._22 = pArray[5];
mat._23 = pArray[6];
mat._24 = pArray[7];
mat._31 = pArray[8];
mat._32 = pArray[9];
mat._33 = pArray[10];
mat._34 = pArray[11];
```

```
DirectX::XMFLOAT3X4 mat;
mat.m[0, 0] = pArray[0];
mat.m[0, 1] = pArray[1];
mat.m[0, 2] = pArray[2];
mat.m[0, 3] = pArray[3];
mat.m[1, 0] = pArray[4];
mat.m[1, 1] = pArray[5];
mat.m[1, 2] = pArray[6];
mat.m[1, 3] = pArray[7];
mat.m[2, 0] = pArray[8];
mat.m[2, 1] = pArray[9];
mat.m[2, 2] = pArray[10];
mat.m[2, 3] = pArray[11];
```

## -see-also

[XMFLOAT3X4 structure](./ns-directxmath-xmfloat3x4.md)
