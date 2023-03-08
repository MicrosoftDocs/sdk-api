---
UID: NF:directxmath.XMVectorSum
title: XMVectorSum function (directxmath.h)
description: Computes the horizontal sum of the components of an XMVECTOR. The horizontal sum is the result of adding each component in the vector together.
helpviewer_keywords: ["Use DirectX..XMVectorSum","XMVectorSum","XMVectorSum method [DirectX Math Support APIs]","dxmath.xmvectorsum"]
old-location: dxmath\xmvectorsum.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorSum(FXMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSum, XMVectorSum, XMVectorSum method [DirectX Math Support APIs], dxmath.xmvectorsum
req.header: directxmath.h
req.include-header: DirectXMath.h
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
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
ms.custom: 19H1
f1_keywords:
 - XMVectorSum
 - directxmath/XMVectorSum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorSum
---

# XMVectorSum function


## -description

Computes the horizontal sum of the components of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. The horizontal sum is the result of adding each component in the vector together.

## -parameters

### -param V [in]

Vector for which to compute the horizontal sum.

## -returns

Returns a vector whose components are the horizontal sum of the components of <i>V</i>.

## -remarks

Note that for SSE/SSE2, horizonal sums require a number of math and shuffle operations. If you enable SSE3 (via defining ``_XM_SSE3_INTRINSICS_``, ``/arch:AVX``, or ``/arch:AVX2``) -or- if using Windows on ARM/ARM64, this function can make use of horizonal sum intrinsics.

> This is new to DirectXMath 3.10

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>
