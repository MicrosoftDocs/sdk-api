---
UID: NF:directxmath.XMScalarASinEst
title: XMScalarASinEst function (directxmath.h)
description: Estimates the arcsine of a floating-point number.
helpviewer_keywords: ["Use DirectX..XMScalarASinEst","XMScalarASinEst","XMScalarASinEst method [DirectX Math Support APIs]","dxmath.xmscalarasinest"]
old-location: dxmath\xmscalarasinest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarASinEst(float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMScalarASinEst, XMScalarASinEst, XMScalarASinEst method [DirectX Math Support APIs], dxmath.xmscalarasinest
f1_keywords:
- directxmath/XMScalarASinEst
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXMath.h
api_name:
- XMScalarASinEst
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMScalarASinEst function


## -description


Estimates the arcsine of a floating-point number.


## -parameters




### -param Value [in]

<b>float</b> value between -1.0f and 1.0f.


## -returns



Returns the inverse sine of <i>Value</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses a 3-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-scalar">DirectXMath Library Scalar Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmscalarasin">XMScalarASin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmscalarsin">XMScalarSin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmscalarsinest">XMScalarSinEst</a>
 

 

