---
UID: NF:directxmath.XMPlaneNearEqual
title: XMPlaneNearEqual function (directxmath.h)
description: Determines whether two planes are nearly equal.
helpviewer_keywords: ["Use DirectX..XMPlaneNearEqual","XMPlaneNearEqual","XMPlaneNearEqual method [DirectX Math Support APIs]","dxmath.xmplanenearequal"]
old-location: dxmath\xmplanenearequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneNearEqual(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneNearEqual, XMPlaneNearEqual, XMPlaneNearEqual method [DirectX Math Support APIs], dxmath.xmplanenearequal
req.header: directxmath.h
req.include-header: 
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
 - XMPlaneNearEqual
 - directxmath/XMPlaneNearEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMPlaneNearEqual
---

# XMPlaneNearEqual function


## -description

Determines whether two planes are nearly equal.

## -parameters

### -param P1 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

### -param P2 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

### -param Epsilon [in]

<b>An XMVECTOR</b> that gives the component-wise tolerance to use when comparing <i>P1</i> and <i>P2</i>.

## -returns

Returns <b>true</b> if <i>P1</i> is nearly equal to <i>P2</i> and <b>false</b> otherwise.

## -remarks

The <code>XMPlaneNearEqual</code> function normalizes the <i>P1</i> and <i>P2</i> parameters before passing them, and the <i>Epsilon</i> parameter, to the <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4nearequal">XMVector4NearEqual</a> function.  For more information about how the calculation is performed, see the <b>XMVector4NearEqual</b> function.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>