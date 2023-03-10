---
UID: NF:directxmath.XMVectorReciprocalSqrt
title: XMVectorReciprocalSqrt function (directxmath.h)
description: Computes the per-component reciprocal square root of a vector.
helpviewer_keywords: ["Use DirectX..XMVectorReciprocalSqrt","XMVectorReciprocalSqrt","XMVectorReciprocalSqrt method [DirectX Math Support APIs]","dxmath.xmvectorreciprocalsqrt"]
old-location: dxmath\xmvectorreciprocalsqrt.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorReciprocalSqrt(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorReciprocalSqrt, XMVectorReciprocalSqrt, XMVectorReciprocalSqrt method [DirectX Math Support APIs], dxmath.xmvectorreciprocalsqrt
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
 - XMVectorReciprocalSqrt
 - directxmath/XMVectorReciprocalSqrt
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
 - XMVectorReciprocalSqrt
---

# XMVectorReciprocalSqrt function


## -description

Computes the per-component reciprocal square root of a vector.

## -parameters

### -param V [in]

Vector whose reciprocal square root is computed.

## -returns

Returns a vector. Each component is the reciprocal square-root of the corresponding component of <i>V</i>.

## -remarks

The reciprocal square-root operation handles special input values as follows.

<table>
<tr>
<th>Input Value</th>
<th>Return Value</th>
</tr>
<tr>
<td>+Infinity</td>
<td>0*</td>
</tr>
<tr>
<td>+0.0f</td>
<td>+Infinity*</td>
</tr>
<tr>
<td>-0.0f</td>
<td>-Infinity*</td>
</tr>
<tr>
<td>&lt; 0.0f</td>
<td>QNaN</td>
</tr>
</table>
 

* Note that due to implementation details, VMX128 returns QNaN in all special cases.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest">XMVectorReciprocalSqrtEst</a>