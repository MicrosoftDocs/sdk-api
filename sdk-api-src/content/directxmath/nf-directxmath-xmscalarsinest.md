---
UID: NF:directxmath.XMScalarSinEst
title: XMScalarSinEst function (directxmath.h)
description: Estimates the sine of a radian angle.
helpviewer_keywords: ["Use DirectX..XMScalarSinEst","XMScalarSinEst","XMScalarSinEst method [DirectX Math Support APIs]","dxmath.xmscalarsinest"]
old-location: dxmath\xmscalarsinest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarSinEst(float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMScalarSinEst, XMScalarSinEst, XMScalarSinEst method [DirectX Math Support APIs], dxmath.xmscalarsinest
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
 - XMScalarSinEst
 - directxmath/XMScalarSinEst
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
 - XMScalarSinEst
---

# XMScalarSinEst function


## -description

Estimates the sine of a radian angle.

## -parameters

### -param Value [in]

<b>float</b> value describing the radian angle.

## -returns

Returns an estimate of the sine of <i>Value</i>.

## -remarks

<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses a 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-scalar">DirectXMath Library Scalar Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmscalarasin">XMScalarASin</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmscalarasinest">XMScalarASinEst</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmscalarsin">XMScalarSin</a>