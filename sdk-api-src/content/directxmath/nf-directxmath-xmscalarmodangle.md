---
UID: NF:directxmath.XMScalarModAngle
title: XMScalarModAngle function (directxmath.h)
description: Computes an angle between -XM_PI and XM_PI.
helpviewer_keywords: ["Use DirectX..XMScalarModAngle","XMScalarModAngle","XMScalarModAngle method [DirectX Math Support APIs]","dxmath.xmscalarmodangle"]
old-location: dxmath\xmscalarmodangle.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarModAngle(float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMScalarModAngle, XMScalarModAngle, XMScalarModAngle method [DirectX Math Support APIs], dxmath.xmscalarmodangle
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
 - XMScalarModAngle
 - directxmath/XMScalarModAngle
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
 - XMScalarModAngle
---

# XMScalarModAngle function


## -description

Computes an angle between -XM_PI and XM_PI.

## -parameters

### -param Value [in]

<b>float</b> value describing the radian angle.

## -returns

Returns an angle greater than or equal to -XM_PI and less than XM_PI that is congruent to <i>Value</i> modulo 2pi.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-scalar">DirectXMath Library Scalar Functions</a>