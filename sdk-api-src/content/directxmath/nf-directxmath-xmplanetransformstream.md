---
UID: NF:directxmath.XMPlaneTransformStream
title: XMPlaneTransformStream function (directxmath.h)
description: Transforms a stream of planes by a given matrix.
helpviewer_keywords: ["Use DirectX..XMPlaneTransformStream","XMPlaneTransformStream","XMPlaneTransformStream method [DirectX Math Support APIs]","dxmath.xmplanetransformstream"]
old-location: dxmath\xmplanetransformstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneTransformStream(XMFLOAT4@,size_t,const XMFLOAT4,size_t,size_t,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneTransformStream, XMPlaneTransformStream, XMPlaneTransformStream method [DirectX Math Support APIs], dxmath.xmplanetransformstream
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
 - XMPlaneTransformStream
 - directxmath/XMPlaneTransformStream
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
 - XMPlaneTransformStream
---

# XMPlaneTransformStream function


## -description

Transforms a stream of planes by a given matrix.

## -parameters

### -param pOutputStream [out]

Address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4">XMFLOAT4</a> in the destination stream. The components of each
        <b>XMFLOAT4</b> are the plane coefficients (A, B, C, D) for the plane equation
        <code>Ax+By+Cz+D=0</code>.

### -param OutputStride [in]

Stride, in bytes, between planes in the destination stream.

### -param pInputStream [in]

Address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4">XMFLOAT4</a> in the stream to be transformed. The components of each
        <b>XMFLOAT4</b> are the plane coefficients (A, B, C, D) for the plane equation
        <code>Ax+By+Cz+D=0</code>.

### -param InputStride [in]

Stride, in bytes, between planes in the input stream.

### -param PlaneCount [in]

Number of planes to transform.

### -param M [in]

Transformation matrix.

## -returns

Returns the address of the first <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4">XMFLOAT4</a> in the destination stream. The components of
       each <b>XMFLOAT4</b> are the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmplanetransform">XMPlaneTransform</a>