---
UID: NF:directxcollision.BoundingFrustum.CreateFromMatrix
title: BoundingFrustum::CreateFromMatrix
description: Creates a BoundingFrustum from the specified projection matrix.
helpviewer_keywords: ["BoundingFrustum interface [DirectX Math Support APIs]","CreateFromMatrix method","BoundingFrustum.CreateFromMatrix","BoundingFrustum::CreateFromMatrix","CreateFromMatrix","CreateFromMatrix method [DirectX Math Support APIs]","CreateFromMatrix method [DirectX Math Support APIs]","BoundingFrustum interface","dxmath.boundingfrustum_createfrommatrix"]
old-location: dxmath\boundingfrustum_createfrommatrix.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.CreateFromMatrix(BoundingFrustum@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: BoundingFrustum interface [DirectX Math Support APIs],CreateFromMatrix method, BoundingFrustum.CreateFromMatrix, BoundingFrustum::CreateFromMatrix, CreateFromMatrix, CreateFromMatrix method [DirectX Math Support APIs], CreateFromMatrix method [DirectX Math Support APIs],BoundingFrustum interface, dxmath.boundingfrustum_createfrommatrix
req.header: directxcollision.h
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
req.namespace: 
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
 - BoundingFrustum::CreateFromMatrix
 - directxcollision/BoundingFrustum::CreateFromMatrix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXCollision.h
api_name:
 - BoundingFrustum.CreateFromMatrix
---

# BoundingFrustum::CreateFromMatrix


## -description

Creates a [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) from the specified perspective projection matrix.

## -parameters

### -param Out [out, ref]

The new [BoundingFrustum](./ns-directxcollision-boundingfrustum.md).

### -param Projection [in]

The projection matrix to create the [BoundingFrustum](./ns-directxcollision-boundingfrustum.md) from.

### -param rhcoords [in]

If set to false (the default), this indicates the projection matrix is in left-handed coordinates. Set it to true if using right-handed coordinates.

> This parameter was added in DirectXMath 3.16.

## -returns

This method does not return a value.

## -remarks

This method is not suitable for use with orthographic projection matricies.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](./ns-directxcollision-boundingfrustum.md)



<a href="https://msdn.microsoft.com/85A76263-92C4-4AF1-BFDE-C68A30CD5583">Methods</a>



<b>Reference</b>
