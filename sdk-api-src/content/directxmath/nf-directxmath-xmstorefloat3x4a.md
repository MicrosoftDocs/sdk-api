---
UID: NF:directxmath.XMStoreFloat3x4A
title: XMStoreFloat3x4A
ms.date: 04/23/2020
description: Stores an [**XMMATRIX**](../directxmath/ns-directxmath-xmmatrix.md) in an [**XMFLOAT3X4A**](../directxmath/ns-directxmath-xmfloat3x4a.md).
tech.root: dxmath
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
 - XMStoreFloat3x4A
 - directxmath/XMStoreFloat3x4A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMStoreFloat3x4A
---

## -description

Stores an [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) in an [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a).

## -parameters

### -param pDestination [out]

Type: **XMFLOAT3X4A \*** 

Pointer to the [**XMFLOAT3X4A**](./ns-directxmath-xmfloat3x4a.md) structure in which to store the data.

### -param M [in]

Type: **[XMMATRIX](./ns-directxmath-xmmatrix.md)**

Matrix containing the data to store.

## -remarks

[**XMFLOAT3X4A**](./ns-directxmath-xmfloat3x4a.md) is a row-major form of the matrix.

To write out column-major data requires that the [**XMMATRIX**](./ns-directxmath-xmmatrix.md) be transposed via  [XMMatrixTranspose](./nf-directxmath-xmmatrixtranspose.md) before calling the store function.

## -see-also

[DirectXMath Library vector store functions](/windows/win32/dxmath/ovw-xnamath-reference-functions-storage)
