---
UID: NF:directxmath.XMVector3UnprojectStream
title: XMVector3UnprojectStream function (directxmath.h)
description: Transforms a stream of 3D vectors from screen space to object space.
helpviewer_keywords: ["Use DirectX..XMVector3UnprojectStream","XMVector3UnprojectStream","XMVector3UnprojectStream method [DirectX Math Support APIs]","dxmath.xmvector3unprojectstream"]
old-location: dxmath\xmvector3unprojectstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3UnprojectStream(XMFLOAT3@,size_t,const XMFLOAT3,size_t,size_t,float,float,float,float,float,float,XMMATRIX,XMMATRIX,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3UnprojectStream, XMVector3UnprojectStream, XMVector3UnprojectStream method [DirectX Math Support APIs], dxmath.xmvector3unprojectstream
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
 - XMVector3UnprojectStream
 - directxmath/XMVector3UnprojectStream
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
 - XMVector3UnprojectStream
---

# XMVector3UnprojectStream function


## -description

Transforms a stream of 3D vectors from screen space to object space.

## -parameters

### -param pOutputStream [out]

Address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the destination stream.

### -param OutputStride [in]

Stride, in bytes, between vectors in the destination stream.

### -param pInputStream [in]

Address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the stream to be transformed. X,Y are in pixels, while Z is 0.0 (at <i>ViewportMinZ</i>) to 1.0 (at <i>ViewportMaxZ</i>).

### -param InputStride [in]

Stride, in bytes, between vectors in the input stream.

### -param VectorCount [in]

Number of vectors to transform.

### -param ViewportX [in]

Pixel coordinate of the upper-left corner of the viewport. Unless you want to render to a subset of the surface, this
        parameter can be set to 0.

### -param ViewportY [in]

Pixel coordinate of the upper-left corner of the viewport on the render-target surface. Unless you want to render to a
        subset of the surface, this parameter can be set to 0.

### -param ViewportWidth [in]

Width dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this parameter
        should be set to the width dimension of the render-target surface.

### -param ViewportHeight [in]

Height dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this parameter
        should be set to the height dimension of the render-target surface.

### -param ViewportMinZ [in]

Together with <i>ViewportMaxZ</i>, value describing the range of depth values into which a scene is to be rendered,
        the minimum and maximum values of the clip volume. Most applications set this value to 0.0f. Clipping is
        performed after applying the projection matrix.

### -param ViewportMaxZ [in]

Together with <i>MinZ</i>, value describing the range of depth values into which a scene is to be rendered, the
        minimum and maximum values of the clip volume. Most applications set this value to 1.0f. Clipping is performed
        after applying the projection matrix.

### -param Projection [in]

Projection matrix.

### -param View [in]

View matrix.

### -param World [in]

World matrix.

## -returns

Returns the address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the destination stream.

## -remarks

The <i>ViewportX</i>, <i>ViewportY</i>, <i>ViewportWidth</i>, and <i>ViewportHeight</i> parameters
   describe the position and dimensions of the viewport on the render-target surface. Usually, applications render to
   the entire target surface; when rendering on a 640*480 surface, these parameters should be 0, 0, 640, and
   480, respectively. The <i>ViewportMinZ</i> and <i>ViewportMaxZ</i> are typically set to 0.0f and 1.0f but can
   be set to other values to achieve specific effects.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector3unproject">XMVector3Unproject</a>