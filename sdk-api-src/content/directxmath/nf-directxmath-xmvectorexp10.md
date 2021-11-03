---
UID: NF:directxmath.XMVectorExp10
title: XMVectorExp10 function (directxmath.h)
description: Computes ten raised to the power for each component.
helpviewer_keywords: ["Use DirectX..XMVectorExp10","XMVectorExp10","XMVectorExp10 method [DirectX Math Support APIs]","dxmath.xmvectorexp10"]
tech.root: dxmath
ms.date: 06/06/2021
ms.keywords: Use DirectX..XMVectorExp10, XMVectorExp10, XMVectorExp10 method [DirectX Math Support APIs], dxmath.xmvectorexp10
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
 - XMVectorExp10
 - directxmath/XMVectorExp10
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
 - XMVectorExp10
---

# XMVectorExp10 function


## -description

Computes ten raised to the power for each component.

## -parameters

### -param V [in]

Vector used for the exponents of base ten.

## -returns

Returns a vector whose components are ten raised to the power of the corresponding component of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
 Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

> This function was added in DirectXMath 3.16


<b>XMVectorExp10</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = powf(10.0f, V.x);
Result.y = powf(10.0f, V.y);
Result.z = powf(10.0f, V.z);
Result.w = powf(10.0f, V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp2">XMVectorExp2</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexpe">XMVectorExpE</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog10">XMVectorLog10</a>
