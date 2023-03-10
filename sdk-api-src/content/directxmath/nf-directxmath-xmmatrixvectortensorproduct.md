---
UID: NF:directxmath.XMMatrixVectorTensorProduct
title: XMMatrixVectorTensorProduct function (directxmath.h)
description: Builds an matrix from two vectors
helpviewer_keywords: ["Use DirectX..XMMatrixVectorTensorProduct","XMMatrixVectorTensorProduct","XMMatrixVectorTensorProduct method [DirectX Math Support APIs]","dxmath.xmmatrixvectortensorproduct"]
tech.root: dxmath
ms.date: 06/06/2021
ms.keywords: Use DirectX..XMMatrixVectorTensorProduct,XMMatrixVectorTensorProduct,XMMatrixVectorTensorProduct method [DirectX Math Support APIs], dxmath.xmmatrixvectortensorproduct
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
req.namespace: Use DirectX.
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: MN
f1_keywords:
 - XMMatrixVectorTensorProduct
 - directxmath/XMMatrixVectorTensorProduct
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
 - XMMatrixVectorTensorProduct
---

# XMMatrixVectorTensorProduct function


## -description

Builds a matrix from two vectors by computing the outer tensor product.

## -parameters

### -param V1 [in]

3D vector.

### -param V2 [in]

3D vector.

## -returns

Returns the outer tensor product of <i>V1</i> and <i>V2</i>.

## -remarks

See [Wikipedia](https://en.wikipedia.org/wiki/Outer_product) for more information on the *outer product*.

> This function was added in DirectXMath 3.15.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>
