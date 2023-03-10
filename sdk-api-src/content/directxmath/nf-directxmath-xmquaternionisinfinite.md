---
UID: NF:directxmath.XMQuaternionIsInfinite
title: XMQuaternionIsInfinite function (directxmath.h)
description: Test whether any component of a quaternion is either positive or negative infinity.
helpviewer_keywords: ["Use DirectX..XMQuaternionIsInfinite","XMQuaternionIsInfinite","XMQuaternionIsInfinite method [DirectX Math Support APIs]","dxmath.xmquaternionisinfinite"]
old-location: dxmath\xmquaternionisinfinite.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionIsInfinite(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionIsInfinite, XMQuaternionIsInfinite, XMQuaternionIsInfinite method [DirectX Math Support APIs], dxmath.xmquaternionisinfinite
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
 - XMQuaternionIsInfinite
 - directxmath/XMQuaternionIsInfinite
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
 - XMQuaternionIsInfinite
---

# XMQuaternionIsInfinite function


## -description

Test whether any component of a quaternion is either positive or negative infinity.

## -parameters

### -param Q [in]

Quaternion to test.

## -returns

Returns true if any component of <i>Q</i> is positive or negative infinity,and false otherwise.

## -remarks

The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>