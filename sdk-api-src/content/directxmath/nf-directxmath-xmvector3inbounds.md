---
UID: NF:directxmath.XMVector3InBounds
title: XMVector3InBounds function (directxmath.h)
description: Tests whether the components of a 3D vector are within set bounds.
helpviewer_keywords: ["Use DirectX..XMVector3InBounds","XMVector3InBounds","XMVector3InBounds method [DirectX Math Support APIs]","dxmath.xmvector3inbounds"]
old-location: dxmath\xmvector3inbounds.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3InBounds(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3InBounds, XMVector3InBounds, XMVector3InBounds method [DirectX Math Support APIs], dxmath.xmvector3inbounds
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
 - XMVector3InBounds
 - directxmath/XMVector3InBounds
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
 - XMVector3InBounds
---

# XMVector3InBounds function


## -description

Tests whether the components of a 3D vector are within set bounds.

## -parameters

### -param V [in]

3D vector to test.

### -param Bounds [in]

3D vector that determines the bounds.

## -returns

Returns true if both the x, y, and z-components of <i>V</i> are within the set bounds, and false otherwise.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
return (V.x <= Bounds.x && V.x >= -Bounds.x) &&
       (V.y <= Bounds.y && V.y >= -Bounds.y) &&
       (V.z <= Bounds.z && V.z >= -Bounds.z);
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>