---
UID: NF:directxmath.XMVector3ClampLengthV
title: XMVector3ClampLengthV function (directxmath.h)
description: Clamps the length of a 3D vector to a given range. (XMVector3ClampLengthV)
helpviewer_keywords: ["Use DirectX..XMVector3ClampLengthV","XMVector3ClampLengthV","XMVector3ClampLengthV method [DirectX Math Support APIs]","dxmath.xmvector3clamplengthv"]
old-location: dxmath\xmvector3clamplengthv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3ClampLengthV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3ClampLengthV, XMVector3ClampLengthV, XMVector3ClampLengthV method [DirectX Math Support APIs], dxmath.xmvector3clamplengthv
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
 - XMVector3ClampLengthV
 - directxmath/XMVector3ClampLengthV
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
 - XMVector3ClampLengthV
---

# XMVector3ClampLengthV function


## -description

Clamps the length of a 3D vector to a given range.

## -parameters

### -param V [in]

3D vector to clamp.

### -param LengthMin [in]

3D vector whose x, y, and z-components are equal to the minimum clamp length. The x, y, and z-components must be greater-than-or-equal to zero.

### -param LengthMax [in]

3D vector whose x, y, and z-components are equal to the minimum clamp length. The x, y, and z-components must be greater-than-or-equal to zero.

## -returns

Returns a 3D vector whose length is clamped to the specified minimum and maximum.

## -remarks

This function is identical to <a href="/windows/win32/api/directxmath/nf-directxmath-xmvector3clamplength">XMVector3ClampLength</a> except that <i>LengthMin</i> and <i>LengthMax</i> are supplied using 3D vectors instead of <b>float</b> values.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>



<a href="/windows/win32/api/directxmath/nf-directxmath-xmvector3clamplength">XMVector3ClampLength</a>
