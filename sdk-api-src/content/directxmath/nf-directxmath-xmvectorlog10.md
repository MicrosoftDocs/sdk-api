---
UID: NF:directxmath.XMVectorLog10
title: XMVectorLog10 function (directxmath.h)
description: Computes the base ten logarithm of each component of a vector.
helpviewer_keywords: ["Use DirectX..XMVectorLog10","XMVectorLog10","XMVectorLog10 method [DirectX Math Support APIs]","dxmath.xmvectorlog10"]
tech.root: dxmath
ms.date: 06/06/2021
ms.keywords: Use DirectX..XMVectorLog10, XMVectorLog10, XMVectorLog10 method [DirectX Math Support APIs], dxmath.xmvectorlog10
req.header: directxmath.h
req.include-header: DirectXMath.h
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
ms.custom: FE
f1_keywords:
 - XMVectorLog10
 - directxmath/XMVectorLog10
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
 - XMVectorLog10
---

# XMVectorLog10 function


## -description

Computes the base ten logarithm of each component of a vector.

## -parameters

### -param V [in]

Vector for which to compute the base ten logarithm.

## -returns

Returns a vector whose components are base ten logarithm of the corresponding components of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

> This function was added in DirectXMath 3.16


<b>XMVectorLog10</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = log10f(V.x);
Result.y = log10f(V.y);
Result.z = log10f(V.z);
Result.w = log10f(V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorloge">XMVectorLogE</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog2">XMVectorLog2</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp10">XMVectorExp10</a>
