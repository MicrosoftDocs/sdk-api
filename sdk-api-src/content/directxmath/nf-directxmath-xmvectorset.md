---
UID: NF:directxmath.XMVectorSet
title: XMVectorSet function (directxmath.h)
description: Creates a vector using four floating-point values.
helpviewer_keywords: ["Use DirectX..XMVectorSet","XMVectorSet","XMVectorSet method [DirectX Math Support APIs]","dxmath.xmvectorset"]
old-location: dxmath\xmvectorset.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.initialization.XMVectorSet(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSet, XMVectorSet, XMVectorSet method [DirectX Math Support APIs], dxmath.xmvectorset
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
 - XMVectorSet
 - directxmath/XMVectorSet
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
 - XMVectorSet
---

# XMVectorSet function


## -description

Creates a vector using four floating-point values.

## -parameters

### -param x [in]

The x component of the vector to return.

### -param y [in]

The y component of the vector to return.

### -param z [in]

The z component of the vector to return.

### -param w [in]

The w component of the vector to return.

## -returns

An instance <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> each of whose four components
(<i>x</i>,<i>y</i>,<i>z</i>, and <i>w</i>) is a
floating-point number with the same value as the corresponding input argument to
<code>XMVectorSet</code>.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR V;
float x,y,z,w;
V.x = x;
V.y = y;
V.z = z;
V.w = w;

return V;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-initialization">Vector Initialization Functions</a>