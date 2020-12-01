---
UID: NF:directxmath.XMVectorTruncate
title: XMVectorTruncate function (directxmath.h)
description: Rounds each component of a vector to the nearest integer value in the direction of zero.
helpviewer_keywords: ["Use DirectX..XMVectorTruncate","XMVectorTruncate","XMVectorTruncate method [DirectX Math Support APIs]","dxmath.xmvectortruncate"]
old-location: dxmath\xmvectortruncate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorTruncate(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorTruncate, XMVectorTruncate, XMVectorTruncate method [DirectX Math Support APIs], dxmath.xmvectortruncate
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
 - XMVectorTruncate
 - directxmath/XMVectorTruncate
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
 - XMVectorTruncate
---

# XMVectorTruncate function


## -description

Rounds each component of a vector to the nearest integer value in the direction of zero.

## -parameters

### -param V [in]

Vector whose components are to be truncated.

## -returns

Returns a vector whose components are rounded to the nearest integer value in the direction of zero.

## -remarks

The return value is computed based on the following logic, which preserves special values (INF,+INF,NaN,-NaN).


```

Result[0] = (fabsf(V[0]) < 8388608.0f) ? ((float)((int32_t)V[0])) : V[0];
Result[1] = (fabsf(V[1]) < 8388608.0f) ? ((float)((int32_t)V[1])) : V[1];
Result[2] = (fabsf(V[2]) < 8388608.0f) ? ((float)((int32_t)V[2])) : V[2];
Result[3] = (fabsf(V[3]) < 8388608.0f) ? ((float)((int32_t)V[3])) : V[3];
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>