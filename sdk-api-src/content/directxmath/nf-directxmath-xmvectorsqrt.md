---
UID: NF:directxmath.XMVectorSqrt
title: XMVectorSqrt function (directxmath.h)
description: Computes the per-component square root of a vector.
helpviewer_keywords: ["Use DirectX..XMVectorSqrt","XMVectorSqrt","XMVectorSqrt method [DirectX Math Support APIs]","dxmath.xmvectorsqrt"]
old-location: dxmath\xmvectorsqrt.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorSqrt(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSqrt, XMVectorSqrt, XMVectorSqrt method [DirectX Math Support APIs], dxmath.xmvectorsqrt
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
 - XMVectorSqrt
 - directxmath/XMVectorSqrt
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
 - XMVectorSqrt
---

# XMVectorSqrt function


## -description

Computes the per-component square root of a vector.

## -parameters

### -param V [in]

Vector whose square root is computed.

## -returns

Returns a vector. Each component is the square-root of the corresponding component of <i>V</i>.

## -remarks

The square-root operation handles special input values as follows.

<table>
<tr>
<th>Input Value</th>
<th>Return Value</th>
</tr>
<tr>
<td>+Infinity</td>
<td>+Infinity</td>
</tr>
<tr>
<td>+0.0f</td>
<td>+0.0f</td>
</tr>
<tr>
<td>-0.0f</td>
<td>-0.0f</td>
</tr>
<tr>
<td>&lt; 0.0f</td>
<td>QNaN</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsqrtest">XMVectorSqrtEst</a>