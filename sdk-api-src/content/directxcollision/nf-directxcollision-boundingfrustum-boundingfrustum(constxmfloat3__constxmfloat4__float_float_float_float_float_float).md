---
UID: NF:directxcollision.BoundingFrustum.BoundingFrustum(constXMFLOAT3&,constXMFLOAT4&,float,float,float,float,float,float)
title: BoundingFrustum::BoundingFrustum(const XMFLOAT3 &,const XMFLOAT4 &,float,float,float,float,float,float)
description: Creates an instance of BoundingFrustum. (overload 2/4)
helpviewer_keywords: ["BoundingFrustum","BoundingFrustum constructor [DirectX Math Support APIs]","BoundingFrustum constructor [DirectX Math Support APIs]","BoundingFrustum interface","BoundingFrustum interface [DirectX Math Support APIs]","BoundingFrustum constructor","BoundingFrustum.BoundingFrustum","BoundingFrustum.BoundingFrustum(const XMFLOAT3 &","const XMFLOAT4 &","float","float","float","float","float","float)","BoundingFrustum.BoundingFrustum(const XMFLOAT3&","const XMFLOAT4&","float","float","float","float","float","float)","BoundingFrustum::BoundingFrustum","BoundingFrustum::BoundingFrustum(const XMFLOAT3 &","const XMFLOAT4 &","float","float","float","float","float","float)","dxmath.boundingfrustum_ctor_2"]
old-location: dxmath\boundingfrustum_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.#ctor(XMFLOAT3,XMFLOAT4,float,float,float,float,float,float)
ms.date: 12/05/2018
ms.keywords: BoundingFrustum, BoundingFrustum constructor [DirectX Math Support APIs], BoundingFrustum constructor [DirectX Math Support APIs],BoundingFrustum interface, BoundingFrustum interface [DirectX Math Support APIs],BoundingFrustum constructor, BoundingFrustum.BoundingFrustum, BoundingFrustum.BoundingFrustum(const XMFLOAT3 &,const XMFLOAT4 &,float,float,float,float,float,float), BoundingFrustum.BoundingFrustum(const XMFLOAT3&,const XMFLOAT4&,float,float,float,float,float,float), BoundingFrustum::BoundingFrustum, BoundingFrustum::BoundingFrustum(const XMFLOAT3 &,const XMFLOAT4 &,float,float,float,float,float,float), dxmath.boundingfrustum_ctor_2
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
 - BoundingFrustum::BoundingFrustum
 - directxcollision/BoundingFrustum::BoundingFrustum
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
 - BoundingFrustum.BoundingFrustum
---

# BoundingFrustum::BoundingFrustum(const XMFLOAT3 &,const XMFLOAT4 &,float,float,float,float,float,float)


## -description

Creates an instance of [BoundingFrustum](./ns-directxcollision-boundingfrustum.md).

## -parameters

### -param _Origin [in, ref]

The origin of the frustum.

### -param _Orientation [in, ref]

The orientation of the frustum.

### -param _RightSlope [in]

The slope of the right side of the frustum.

### -param _LeftSlope [in]

The slope of the left side of the frustum.

### -param _TopSlope [in]

The slope of the top of the frustum.

### -param _BottomSlope [in]

The slope of the bottom of the frustum.

### -param _Near [in]

The distance of the near plane from the origin of the frustum.

### -param _Far [in]

The distance of the far plane from the origin of the frustum.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](./ns-directxcollision-boundingfrustum.md)



<a href="https://msdn.microsoft.com/3b278210-3d55-4a2b-879d-942e3bc9800c">Constructors</a>



<b>Reference</b>
