---
UID: NF:directxmath.XMQuaternionSquadV
title: XMQuaternionSquadV function (directxmath.h)
description: Interpolates between four unit quaternions, using spherical quadrangle interpolation. (XMQuaternionSquadV)
helpviewer_keywords: ["Use DirectX..XMQuaternionSquadV","XMQuaternionSquadV","XMQuaternionSquadV method [DirectX Math Support APIs]","dxmath.xmquaternionsquadv"]
old-location: dxmath\xmquaternionsquadv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionSquadV(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionSquadV, XMQuaternionSquadV, XMQuaternionSquadV method [DirectX Math Support APIs], dxmath.xmquaternionsquadv
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
 - XMQuaternionSquadV
 - directxmath/XMQuaternionSquadV
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
 - XMQuaternionSquadV
---

# XMQuaternionSquadV function


## -description

Interpolates between four unit quaternions, using spherical quadrangle interpolation.

## -parameters

### -param Q0 [in]

First unit quaternion.

### -param Q1 [in]

Second unit quaternion.

### -param Q2 [in]

Third unit quaternion.

### -param Q3 [in]

Fourth unit quaternion.

### -param T [in]

Interpolation control factor. All components of this vector must be the same.

## -returns

Returns the interpolated quaternion. If <i>Q0</i>, <i>Q1</i>, <i>Q2</i>, and <i>Q3</i> are not unit
       quaternions, the resulting interpolation is undefined.

## -remarks

The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquad">XMQuaternionSquad</a> except that
   <i>T</i> is supplied using a 4D vector instead of a <b>float</b> value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquad">XMQuaternionSquad</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquadsetup">XMQuaternionSquadSetup</a>
