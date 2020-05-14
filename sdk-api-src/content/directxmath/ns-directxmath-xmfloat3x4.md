---
UID: NS:directxmath.XMFLOAT3X4
title: XMFLOAT3X4
description: A 3x4 column-major matrix containing 32-bit floating-point components.
ms.date: 04/21/2020
helpviewer_keywords: ["XMFLOAT3X4","XMFLOAT3X4 structure [DirectX Math Support APIs]","directxmath/XMFLOAT3X4","dxmath.xmfloat3x3"]
tech.root: dxmath
f1_keywords:
- directxmath/XMFLOAT3X4
dev_langs:
- c++
req.construct-type: structure
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- apiref
- kbSyntax
api_type:
- HeaderDef
api_location:
- directxmath.h
api_name:
- XMFLOAT3X4
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

A 3x4 column-major matrix containing 32-bit floating-point components.

> [!NOTE]
> See [Library internals](/windows/win32/dxmath/pg-xnamath-internals) for info about equivalent [D3DDECLTYPE](/windows/win32/direct3d9/d3ddecltype), [D3DFORMAT](/windows/win32/direct3d9/d3dformat), and [DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) objects.

## -struct-fields

### -field _11
An element of the matrix.

### -field _12
An element of the matrix.

### -field _13
An element of the matrix.

### -field _14
An element of the matrix.

### -field _21
An element of the matrix.

### -field _22
An element of the matrix.

### -field _23
An element of the matrix.

### -field _24
An element of the matrix.

### -field _31
An element of the matrix.

### -field _32
An element of the matrix.

### -field _33
An element of the matrix.

### -field _34
An element of the matrix.

### -field m
A 3x4 array representing the matrix.

### -field f
A 12-element (3*4) array representing the matrix.

## -remarks

The scalar members of **XMFLOAT3X3** have names that follow the form *_\<row_number\>\<column_number\>* (for example, *_11*). They provide 1-based indexing, where *row_number* specifies the 1-based matrix row (ranging from 1 to 3), and *column_number* specifies the 1-based matrix column (ranging from 1 to 4).

The member *m* is a 2-dimensional 3x4 array. It provides 0-based indexing of the structure's matrix. When accessing *m\[\<row_index\>, \<column_index\>\]*, *\<row_index\>* ranges from 0 to 2, and *\<column_index\>* ranges from 0 to 3.

You can load an [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) from an **XMFLOAT3X4** by using [XMLoadFloat3x4](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x4).

You can store an [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into an **XMFLOAT3X4** by using [XMStoreFloat3x4](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x4).

## -see-also
[DirectXMath Library structures](/windows/win32/dxmath/ovw-xnamath-reference-structures)