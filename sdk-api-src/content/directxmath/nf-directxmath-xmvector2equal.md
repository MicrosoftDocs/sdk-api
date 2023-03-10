---
UID: NF:directxmath.XMVector2Equal
title: XMVector2Equal function (directxmath.h)
description: Tests whether two 2D vectors are equal.
helpviewer_keywords: ["Use DirectX..XMVector2Equal","XMVector2Equal","XMVector2Equal method [DirectX Math Support APIs]","dxmath.xmvector2equal"]
old-location: dxmath\xmvector2equal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector2Equal(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2Equal, XMVector2Equal, XMVector2Equal method [DirectX Math Support APIs], dxmath.xmvector2equal
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
 - XMVector2Equal
 - directxmath/XMVector2Equal
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
 - XMVector2Equal
---

# XMVector2Equal function


## -description

Tests whether two 2D vectors are equal.

## -parameters

### -param V1 [in]

2D vector.

### -param V2 [in]

2D vector.

## -returns

Returns true if the 2D vectors are equal and false otherwise.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
return ( V1.x == V2.x && V1.y == V2.y );
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-comparison">DirectXMath Library 2D Vector Comparison Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2equalr">XMVector2EqualR</a>