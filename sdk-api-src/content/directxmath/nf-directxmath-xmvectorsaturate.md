---
UID: NF:directxmath.XMVectorSaturate
title: XMVectorSaturate function (directxmath.h)
description: Saturates each component of a vector to the range 0.0f to 1.0f.
helpviewer_keywords: ["Use DirectX..XMVectorSaturate","XMVectorSaturate","XMVectorSaturate method [DirectX Math Support APIs]","dxmath.xmvectorsaturate"]
old-location: dxmath\xmvectorsaturate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorSaturate(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSaturate, XMVectorSaturate, XMVectorSaturate method [DirectX Math Support APIs], dxmath.xmvectorsaturate
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
 - XMVectorSaturate
 - directxmath/XMVectorSaturate
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
 - XMVectorSaturate
---

# XMVectorSaturate function


## -description

Saturates each component of a vector to the range 0.0f to 1.0f.

## -parameters

### -param V [in]

Vector to saturate.

## -returns

Returns a vector, each of whose components are saturated.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = min(max(V1.x, 0.0f), 1.0f);
Result.y = min(max(V1.y, 0.0f), 1.0f);
Result.z = min(max(V1.z, 0.0f), 1.0f);
Result.w = min(max(V1.w, 0.0f), 1.0f);

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>