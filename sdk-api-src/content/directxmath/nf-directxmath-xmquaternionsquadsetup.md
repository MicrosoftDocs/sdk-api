---
UID: NF:directxmath.XMQuaternionSquadSetup
title: XMQuaternionSquadSetup function (directxmath.h)
description: Provides addresses of setup control points for spherical quadrangle interpolation.
helpviewer_keywords: ["Use DirectX..XMQuaternionSquadSetup","XMQuaternionSquadSetup","XMQuaternionSquadSetup method [DirectX Math Support APIs]","dxmath.xmquaternionsquadsetup"]
old-location: dxmath\xmquaternionsquadsetup.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionSquadSetup(XMVECTOR@,XMVECTOR@,XMVECTOR@,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionSquadSetup, XMQuaternionSquadSetup, XMQuaternionSquadSetup method [DirectX Math Support APIs], dxmath.xmquaternionsquadsetup
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
 - XMQuaternionSquadSetup
 - directxmath/XMQuaternionSquadSetup
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
 - XMQuaternionSquadSetup
---

# XMQuaternionSquadSetup function


## -description

Provides addresses of setup control points for spherical quadrangle interpolation.

## -parameters

### -param pA [out]

Address of first setup quaternion.

### -param pB [out]

Address of first setup quaternion.

### -param pC [out]

Address of first setup quaternion.

### -param Q0 [in]

First quaternion.

### -param Q1 [in]

Second quaternion.

### -param Q2 [in]

Third quaternion.

### -param Q3 [in]

Fourth quaternion.

## -returns

None.

## -remarks

The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

The results returned in <i>pA</i>, <i>pB</i>, and <i>pC</i> are used as the inputs to the <i>Q1</i>,
   <i>Q2</i>, and <i>Q3</i> parameters of
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquad">XMQuaternionSquad</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquad">XMQuaternionSquad</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionsquadv">XMQuaternionSquadV</a>