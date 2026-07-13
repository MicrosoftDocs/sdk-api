---
UID: NF:directxmath.XMFLOAT3X4.operator-function-call
title: XMFLOAT3X4::operator()
ms.date: 04/22/2020
description: Returns a copy of a matrix element of an **XMFLOAT3X4**, specified by row and column arguments.
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
 - XMFLOAT3X4::operator()
 - directxmath/XMFLOAT3X4::operator()
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
 - XMFLOAT3X4::operator()
---

## -description

Returns a copy of a matrix element of an **XMFLOAT3X4**, specified by row and column arguments.

## -parameters

### -param Row

Type: **size_t**

The 0-based row number of the matrix element to retrieve.

### -param Column

Type: **size_t**

The 0-based column number of the matrix element to retrieve.

## -returns

Type: **float &**

An lvalue reference to the specified element.

## Examples

Because an lvalue reference to the matrix element is returned, you can use this operator to update the value of an element.

The code example below shows two different ways of setting *mat.m\[2,3\]* (or, equivalently, *mat._34*) to the value 42.0.

```cpp
DirectX::XMFLOAT4X3 mat;

float& a{ mat(2, 3) };
a = 42.0;

mat(2, 3) = 42.0;
```

## -remarks

## -see-also

[XMFLOAT3X4 structure](./ns-directxmath-xmfloat3x4.md)
