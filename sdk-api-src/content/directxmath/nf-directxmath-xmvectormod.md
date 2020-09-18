---
UID: NF:directxmath.XMVectorMod
title: XMVectorMod function (directxmath.h)
description: Computes the per-component floating-point remainder of the quotient of two vectors.
helpviewer_keywords: ["Use DirectX..XMVectorMod","XMVectorMod","XMVectorMod method [DirectX Math Support APIs]","dxmath.xmvectormod"]
old-location: dxmath\xmvectormod.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorMod(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorMod, XMVectorMod, XMVectorMod method [DirectX Math Support APIs], dxmath.xmvectormod
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
 - XMVectorMod
 - directxmath/XMVectorMod
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
 - XMVectorMod
---

# XMVectorMod function


## -description

Computes the per-component floating-point remainder of the quotient of two vectors.

## -parameters

### -param V1 [in]

Vector dividend.

### -param V2 [in]

Vector divisor.

## -returns

Returns a vector whose components are the floating-point remainders of the divisions.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = fmod(V1.x, V2.x);
Result.y = fmod(V1.y, V2.y);
Result.z = fmod(V1.z, V2.z);
Result.w = fmod(V1.w, V2.w);

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>