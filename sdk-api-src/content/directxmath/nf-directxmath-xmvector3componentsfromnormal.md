---
UID: NF:directxmath.XMVector3ComponentsFromNormal
title: XMVector3ComponentsFromNormal function (directxmath.h)
description: Using a reference normal vector, splits a 3D vector into components that are parallel and perpendicular to the normal.
helpviewer_keywords: ["Use DirectX..XMVector3ComponentsFromNormal","XMVector3ComponentsFromNormal","XMVector3ComponentsFromNormal method [DirectX Math Support APIs]","dxmath.xmvector3componentsfromnormal"]
old-location: dxmath\xmvector3componentsfromnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3ComponentsFromNormal(XMVECTOR@,XMVECTOR@,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3ComponentsFromNormal, XMVector3ComponentsFromNormal, XMVector3ComponentsFromNormal method [DirectX Math Support APIs], dxmath.xmvector3componentsfromnormal
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
 - XMVector3ComponentsFromNormal
 - directxmath/XMVector3ComponentsFromNormal
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
 - XMVector3ComponentsFromNormal
---

# XMVector3ComponentsFromNormal function


## -description

Using a reference normal vector, splits a 3D vector into components that are parallel and perpendicular to the normal.

## -parameters

### -param pParallel [out]

Address of the component of <i>V</i> that is parallel to <i>Normal</i>.

### -param pPerpendicular [out]

Address of the component of <i>V</i> that is perpendicular to <i>Normal</i>.

### -param V [in]

3D vector to break into components.

### -param Normal [in]

3D reference normal vector.

## -returns

None.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>