---
UID: NF:directxmath.XMMatrixShadow
title: XMMatrixShadow function (directxmath.h)
description: Builds a transformation matrix that flattens geometry into a plane.
helpviewer_keywords: ["Use DirectX..XMMatrixShadow","XMMatrixShadow","XMMatrixShadow method [DirectX Math Support APIs]","dxmath.xmmatrixshadow"]
old-location: dxmath\xmmatrixshadow.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixShadow(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixShadow, XMMatrixShadow, XMMatrixShadow method [DirectX Math Support APIs], dxmath.xmmatrixshadow
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
 - XMMatrixShadow
 - directxmath/XMMatrixShadow
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
 - XMMatrixShadow
---

# XMMatrixShadow function


## -description

Builds a transformation matrix that flattens geometry into a plane.

## -parameters

### -param ShadowPlane [in]

Reference plane.

### -param LightPosition [in]

4D vector describing the light's position. If the light's w-component is 0.0f, the ray from the origin to the light represents a directional light. If it is 1.0f, the light is a point light.

## -returns

Returns the transformation matrix that flattens the geometry into the plane <i>ShadowPlane</i>.

## -remarks

This function is useful for forming planar-projected shadows from a light source.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>