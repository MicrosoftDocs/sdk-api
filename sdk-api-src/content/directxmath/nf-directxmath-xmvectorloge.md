---
UID: NF:directxmath.XMVectorLogE
title: XMVectorLogE function (directxmath.h)
description: Computes the base e logarithm of each component of a vector.
helpviewer_keywords: ["Use DirectX..XMVectorLogE","XMVectorLogE","XMVectorLogE method [DirectX Math Support APIs]","dxmath.xmvectorloge"]
old-location: dxmath\xmvectorloge.htm
tech.root: dxmath
ms.assetid: C092B786-BAB8-4F8F-95D2-3C23F59EF064
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorLogE, XMVectorLogE, XMVectorLogE method [DirectX Math Support APIs], dxmath.xmvectorloge
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
 - XMVectorLogE
 - directxmath/XMVectorLogE
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
 - XMVectorLogE
---

# XMVectorLogE function


## -description

Computes the base e logarithm of each component of a vector.The base e logarithm is also known as the natural logarithm.

## -parameters

### -param V [in]

Vector for which to compute the base e logarithm.

## -returns

Returns a vector whose components are base e logarithm of the corresponding components of <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorLogE</b> is new for DirectXMath version 3.05.

It's similar to the existing <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog">XMVectorLog</a> function for Windows 8, but computes base e instead of base 2.


<b>XMVectorLogE</b> is implemented like this:


``` syntax

XMVECTOR Result;

Result.x = logf(V.x);
Result.y = logf(V.y);
Result.z = logf(V.z);
Result.w = logf(V.w);

return Result;

```


## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>




<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog2">XMVectorLog2</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorlog10">XMVectorLog10</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorexpe">XMVectorExpE</a>
