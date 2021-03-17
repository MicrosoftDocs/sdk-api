---
UID: NF:directxmath.XMVector3Project
title: XMVector3Project function (directxmath.h)
description: Project a 3D vector from object space into screen space.
helpviewer_keywords: ["Use DirectX..XMVector3Project","XMVector3Project","XMVector3Project method [DirectX Math Support APIs]","dxmath.xmvector3project"]
old-location: dxmath\xmvector3project.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3Project(XMVECTOR,float,float,float,float,float,float,XMMATRIX,XMMATRIX,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Project, XMVector3Project, XMVector3Project method [DirectX Math Support APIs], dxmath.xmvector3project
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
 - XMVector3Project
 - directxmath/XMVector3Project
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
 - XMVector3Project
---

# XMVector3Project function


## -description

Project a 3D vector from object space into screen space.

## -parameters

### -param V [in]

3D vector in object space that will be projected into screen space.

### -param ViewportX [in]

Pixel coordinate of the upper-left corner of the viewport. Unless you want to render to a subset of the surface, this parameter can be set to 0.

### -param ViewportY [in]

Pixel coordinate of the upper-left corner of the viewport on the render-target surface. Unless you want to render to a subset of the surface, this parameter can be set to 0.

### -param ViewportWidth [in]

Width dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this parameter should be set to the width dimension of the render-target surface.

### -param ViewportHeight [in]

Height dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this parameter should be set to the height dimension of the render-target surface.

### -param ViewportMinZ [in]

Together with <i>ViewportMaxZ</i>, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume. Most applications set this value to 0.0f. Clipping is performed after applying the projection matrix.

### -param ViewportMaxZ [in]

Together with <i>MinZ</i>, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume. Most applications set this value to 1.0f. Clipping is performed after applying the projection matrix.

### -param Projection [in]

Projection matrix.

### -param View [in]

View matrix.

### -param World [in]

World matrix.

## -returns

Returns a vector in screen space.

## -remarks

The <i>ViewportX</i>, <i>ViewportY</i>, <i>ViewportWidth</i>, and <i>ViewportHeight</i> parameters describe the position and dimensions of the viewport on the render-target surface. Usually, applications render to the entire target surface; when rendering on a 640*480 surface, these parameters should be 0, 0, 640, and 480, respectively. The <i>ViewportMinZ</i> and <i>ViewportMaxZ</i> are typically set to 0.0f and 1.0f but can be set to other values to achieve specific effects.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector3projectstream">XMVector3ProjectStream</a>