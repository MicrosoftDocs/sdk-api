---
UID: NF:directxmath.XMScalarNearEqual
title: XMScalarNearEqual function (directxmath.h)
description: Determines if two floating-point values are nearly equal.
helpviewer_keywords: ["Use DirectX..XMScalarNearEqual","XMScalarNearEqual","XMScalarNearEqual method [DirectX Math Support APIs]","dxmath.xmscalarnearequal"]
old-location: dxmath\xmscalarnearequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarNearEqual(float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMScalarNearEqual, XMScalarNearEqual, XMScalarNearEqual method [DirectX Math Support APIs], dxmath.xmscalarnearequal
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
 - XMScalarNearEqual
 - directxmath/XMScalarNearEqual
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
 - XMScalarNearEqual
---

# XMScalarNearEqual function


## -description

Determines if two floating-point values are nearly equal.

## -parameters

### -param S1 [in]

First floating-point value to compare.

### -param S2 [in]

Second floating-point value to compare.

### -param Epsilon [in]

Tolerance to use when comparing <i>S1</i> and <i>S2</i>.

## -returns

Returns true if the absolute value of the difference between <i>S1</i> and <i>S2</i> is less than or equal to <i>Epsilon</i>. Returns false otherwise.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-scalar">DirectXMath Library Scalar Functions</a>