---
UID: NF:directxmath.XMVector3Unproject
title: XMVector3Unproject function (directxmath.h)
description: Projects a 3D vector from screen space into object space.helpviewer_keywords: ["Use DirectX..XMVector3Unproject","XMVector3Unproject","XMVector3Unproject method [DirectX Math Support APIs]","dxmath.xmvector3unproject"]
old-location: dxmath\xmvector3unproject.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3Unproject(XMVECTOR,float,float,float,float,float,float,XMMATRIX,XMMATRIX,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Unproject, XMVector3Unproject, XMVector3Unproject method [DirectX Math Support APIs], dxmath.xmvector3unproject
f1_keywords:
- directxmath/XMVector3Unproject
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxmathvector.inl
api_name:
- XMVector3Unproject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3Unproject function


## -description


Projects a 3D vector from screen space into object space.


## -parameters




### -param V [in]

3D vector in screen space that will be projected into object space. X and Y are in pixels, while Z is 0.0 (at <i>ViewportMinZ</i>) to 1.0 (at <i>ViewportMaxZ</i>).


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



Returns a vector in object space.




## -remarks



The <i>ViewportX</i>, <i>ViewportY</i>, <i>ViewportWidth</i>, and <i>ViewportHeight</i> parameters describe the position and dimensions of the viewport on the render-target surface. Usually, applications render to the entire target surface; when rendering on a 640*480 surface, these parameters should be 0, 0, 640, and 480, respectively. The <i>ViewportMinZ</i> and <i>ViewportMaxZ</i> are typically set to 0.0f and 1.0f but can be set to other values to achieve specific effects.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvector3unprojectstream">XMVector3UnprojectStream</a>
 

 

