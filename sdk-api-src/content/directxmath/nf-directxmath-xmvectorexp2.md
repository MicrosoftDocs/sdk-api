---
UID: NF:directxmath.XMVectorExp2
title: XMVectorExp2 function (directxmath.h)
description: Computes two raised to the power for each component.
helpviewer_keywords: ["Use DirectX..XMVectorExp2","XMVectorExp2","XMVectorExp2 method [DirectX Math Support APIs]","dxmath.xmvectorexp2"]
old-location: dxmath\xmvectorexp2.htm
tech.root: dxmath
ms.assetid: 1B04528B-532B-4555-B027-D5EC33DD9843
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorExp2, XMVectorExp2, XMVectorExp2 method [DirectX Math Support APIs], dxmath.xmvectorexp2
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
 - XMVectorExp2
 - directxmath/XMVectorExp2
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
 - XMVectorExp2
---

# XMVectorExp2 function


## -description

Computes two raised to the power for each component.

## -parameters

### -param V [in]

Vector used for the exponents of base two.

## -returns

Returns a vector whose components are two raised to the power of the corresponding component of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorExp2</b> is new for DirectXMath version 3.05, but it's just a renamed version of the existing <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp">XMVectorExp</a> function for Windows 8.



<b>XMVectorExp2</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = exp2f(V.x);
Result.y = exp2f(V.y);
Result.z = exp2f(V.z);
Result.w = exp2f(V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexpe">XMVectorExpE</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp10">XMVectorExp10</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog2">XMVectorLog2</a>
