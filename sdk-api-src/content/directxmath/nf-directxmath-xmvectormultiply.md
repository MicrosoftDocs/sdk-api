---
UID: NF:directxmath.XMVectorMultiply
title: XMVectorMultiply function (directxmath.h)
description: Computes the per-component product of two vectors.
helpviewer_keywords: ["Use DirectX..XMVectorMultiply","XMVectorMultiply","XMVectorMultiply method [DirectX Math Support APIs]","dxmath.xmvectormultiply"]
old-location: dxmath\xmvectormultiply.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorMultiply(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorMultiply, XMVectorMultiply, XMVectorMultiply method [DirectX Math Support APIs], dxmath.xmvectormultiply
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
 - XMVectorMultiply
 - directxmath/XMVectorMultiply
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
 - XMVectorMultiply
---

# XMVectorMultiply function


## -description

Computes the per-component product of two vectors.

## -parameters

### -param V1 [in]

First vector to multiply.

### -param V2 [in]

Second vector to multiply.

## -returns

Returns a vector, each of whose components is the product of the corresponding components of <i>V1</i> and <i>V2</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>