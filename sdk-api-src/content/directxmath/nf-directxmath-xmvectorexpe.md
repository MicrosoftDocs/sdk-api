---
UID: NF:directxmath.XMVectorExpE
title: XMVectorExpE function (directxmath.h)
description: Computes e (~2.71828) raised to the power for each component.
helpviewer_keywords: ["Use DirectX..XMVectorExpE","XMVectorExpE","XMVectorExpE method [DirectX Math Support APIs]","dxmath.xmvectorexpe"]
old-location: dxmath\xmvectorexpe.htm
tech.root: dxmath
ms.assetid: C4A5E4E0-56CC-46E3-87C5-CA99EF512B11
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorExpE, XMVectorExpE, XMVectorExpE method [DirectX Math Support APIs], dxmath.xmvectorexpe
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
 - XMVectorExpE
 - directxmath/XMVectorExpE
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
 - XMVectorExpE
---

# XMVectorExpE function


## -description

Computes e (~2.71828) raised to the power for each component.

## -parameters

### -param V [in]

Vector used for the exponents of base e.

## -returns

Returns a vector whose components are e raised to the power of the corresponding component of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorExpE</b> is new for DirectXMath version 3.05.

It's similar to the existing <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp">XMVectorExp</a> function for Windows 8, but computes base e instead of base 2.


<b>XMVectorExpE</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = expf(V.x);
Result.y = expf(V.y);
Result.z = expf(V.z);
Result.w = expf(V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp2">XMVectorExp2</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexp10">XMVectorExp10</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorloge">XMVectorLogE</a>
