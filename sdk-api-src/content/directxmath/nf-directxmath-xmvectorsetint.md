---
UID: NF:directxmath.XMVectorSetInt
title: XMVectorSetInt function (directxmath.h)
description: Creates a vector with unsigned integer components.
helpviewer_keywords: ["Use DirectX..XMVectorSetInt","XMVectorSetInt","XMVectorSetInt method [DirectX Math Support APIs]","dxmath.xmvectorsetint"]
old-location: dxmath\xmvectorsetint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.initialization.XMVectorSetInt(uint32_t,uint32_t,uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetInt, XMVectorSetInt, XMVectorSetInt method [DirectX Math Support APIs], dxmath.xmvectorsetint
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
 - XMVectorSetInt
 - directxmath/XMVectorSetInt
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
 - XMVectorSetInt
---

# XMVectorSetInt function


## -description

Creates a vector with unsigned integer components.

## -parameters

### -param x [in]

<b>uint32_t</b> value to assign to the x-component of the returned vector.

### -param y [in]

<b>uint32_t</b> value to assign to the y-component of the returned vector.

### -param z [in]

<b>uint32_t</b> value to assign to the z-component of the returned vector.

### -param w [in]

<b>uint32_t</b> value to assign to the w-component of the returned vector.

## -returns

An instance <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> each of whose four components (<i>x</i>,<i>y</i>,<i>z</i>, and <i>w</i>) is an integer with the same value as the corresponding input argument to <code>XMVectorSetInt</code>.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR V;
uint32_t x,y,z,w;
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