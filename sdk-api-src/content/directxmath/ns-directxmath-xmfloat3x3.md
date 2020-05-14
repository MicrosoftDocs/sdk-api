---
UID: NS:directxmath.XMFLOAT3X3
title: XMFLOAT3X3 (directxmath.h)
description: A 3x3 floating-point matrix.
helpviewer_keywords: ["XMFLOAT3X3","XMFLOAT3X3 structure [DirectX Math Support APIs]","directxmath/XMFLOAT3X3","dxmath.xmfloat3x3"]
old-location: dxmath\xmfloat3x3.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT3X3
ms.date: 12/05/2018
ms.keywords: XMFLOAT3X3, XMFLOAT3X3 structure [DirectX Math Support APIs], directxmath/XMFLOAT3X3, dxmath.xmfloat3x3
f1_keywords:
- directxmath/XMFLOAT3X3
dev_langs:
- c++
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
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectXMath.h
api_name:
- XMFLOAT3X3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

A 3x3 floating-point matrix.

> [!NOTE]
> See [Library internals](/windows/win32/dxmath/pg-xnamath-internals) for info about equivalent [D3DDECLTYPE](/windows/win32/direct3d9/d3ddecltype), [D3DFORMAT](/windows/win32/direct3d9/d3dformat), and [DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) objects.

## -struct-fields

### -field _11

An element of the matrix.

### -field _12

An element of the matrix.

### -field _13

An element of the matrix.

### -field _21

An element of the matrix.

### -field _22

An element of the matrix.

### -field _23

An element of the matrix.

### -field _31

An element of the matrix.

### -field _32

An element of the matrix.

### -field _33

An element of the matrix.

### -field m

A 2-dimensional 3x3 array representing the matrix.

## -remarks

The scalar members of **XMFLOAT3X3** have names that follow the form *_\<row_number\>\<column_number\>* (for example, *_11*). They provide 1-based indexing, where *row_number* specifies the 1-based matrix row (ranging from 1 to 3), and *column_number* specifies the 1-based matrix column (ranging from 1 to 3).

The member *m* is a 2-dimensional 3x3 array. It provides 0-based indexing of the structure's matrix. When accessing *m\[\<row_index\>, \<column_index\>\]*, *\<row_index\>* ranges from 0 to 2, and *\<column_index\>* ranges from 0 to 2.

You can load an [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) from an **XMFLOAT3X3** by using [XMLoadFloat3x3](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3).

You can store an [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into an **XMFLOAT3X3** by using [XMStoreFloat3x3](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3).

## -see-also
[DirectXMath Library structures](/windows/win32/dxmath/ovw-xnamath-reference-structures)