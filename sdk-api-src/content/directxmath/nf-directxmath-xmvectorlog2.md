---
UID: NF:directxmath.XMVectorLog2
title: XMVectorLog2 function (directxmath.h)
description: Computes the base two logarithm of each component of a vector.
helpviewer_keywords: ["Use DirectX..XMVectorLog2","XMVectorLog2","XMVectorLog2 method [DirectX Math Support APIs]","dxmath.xmvectorlog2"]
old-location: dxmath\xmvectorlog2.htm
tech.root: dxmath
ms.assetid: 92C911B4-5BC7-443D-BCBB-F4838E24E607
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorLog2, XMVectorLog2, XMVectorLog2 method [DirectX Math Support APIs], dxmath.xmvectorlog2
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
 - XMVectorLog2
 - directxmath/XMVectorLog2
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
 - XMVectorLog2
---

# XMVectorLog2 function


## -description

Computes the base two logarithm of each component of a vector.

## -parameters

### -param V [in]

Vector for which to compute the base two logarithm.

## -returns

Returns a vector whose components are base two logarithm of the corresponding components of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorLog2</b> is new for DirectXMath version 3.05, but it's just a renamed version of the existing <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog">XMVectorLog</a> function for Windows 8.



<b>XMVectorLog2</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = log2f(V.x);
Result.y = log2f(V.y);
Result.z = log2f(V.z);
Result.w = log2f(V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorloge">XMVectorLogE</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog10">XMVectorLog10</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp2">XMVectorExp2</a>
