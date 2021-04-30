---
UID: NF:directxmath.XMVectorPow
title: XMVectorPow function (directxmath.h)
description: Computes V1 raised to the power of V2.
helpviewer_keywords: ["Use DirectX..XMVectorPow","XMVectorPow","XMVectorPow method [DirectX Math Support APIs]","dxmath.xmvectorpow"]
old-location: dxmath\xmvectorpow.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorPow(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorPow, XMVectorPow, XMVectorPow method [DirectX Math Support APIs], dxmath.xmvectorpow
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
 - XMVectorPow
 - directxmath/XMVectorPow
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
 - XMVectorPow
---

# XMVectorPow function


## -description

Computes <i>V1</i> raised to the power of <i>V2</i>.

## -parameters

### -param V1 [in]

First vector.

### -param V2 [in]

Second vector.

## -returns

Returns a vector. Each component is the corresponding component of <i>V1</i> raised to the power of the
          corresponding component in <i>V2</i>.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = pow(V1.x, V2.x);
Result.y = pow(V1.y, V2.y);
Result.z = pow(V1.z, V2.z);
Result.w = pow(V1.w, V2.w);

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>