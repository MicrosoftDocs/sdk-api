---
UID: NF:directxmath.XMFLOAT3X4.operator-function-call(size_t,size_t)
title: XMFLOAT3X4::operator()(size_t,size_t)
ms.date: 04/22/2020
description: Returns a reference to a matrix element of an **XMFLOAT3X4**, specified by row and column arguments.
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

Returns a reference to a matrix element of an **XMFLOAT3X4**, specified by row and column arguments.

## -parameters

### -param Row

Type: **size_t**

The 0-based row number of the matrix element to retrieve.

### -param Column

Type: **size_t**

The 0-based column number of the matrix element to retrieve.

## -returns

Type: **float**

A copy of the specified element.

## -remarks

## -see-also

[XMFLOAT3X4 structure](./ns-directxmath-xmfloat3x4.md)
