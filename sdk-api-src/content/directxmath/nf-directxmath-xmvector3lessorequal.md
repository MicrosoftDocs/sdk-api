---
UID: NF:directxmath.XMVector3LessOrEqual
title: XMVector3LessOrEqual function (directxmath.h)
description: Tests whether one 3D vector is less-than-or-equal-to another 3D vector.
helpviewer_keywords: ["Use DirectX..XMVector3LessOrEqual","XMVector3LessOrEqual","XMVector3LessOrEqual method [DirectX Math Support APIs]","dxmath.xmvector3lessorequal"]
old-location: dxmath\xmvector3lessorequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector3LessOrEqual(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3LessOrEqual, XMVector3LessOrEqual, XMVector3LessOrEqual method [DirectX Math Support APIs], dxmath.xmvector3lessorequal
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
 - XMVector3LessOrEqual
 - directxmath/XMVector3LessOrEqual
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
 - XMVector3LessOrEqual
---

# XMVector3LessOrEqual function


## -description

Tests whether one 3D vector is less-than-or-equal-to another 3D vector.

## -parameters

### -param V1 [in]

3D vector.

### -param V2 [in]

3D vector.

## -returns

Returns true if <i>V1</i> is less-than-or-equal-to <i>V2</i> and false otherwise. See the remarks section.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
return ( V1.x <= V2.x && V1.y <= V2.y &&
         V1.z <= V2.z );
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-comparison">DirectXMath Library 3D Vector Comparison Functions</a>