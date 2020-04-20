---
UID: NF:directxmath.XMVectorSinEst
title: XMVectorSinEst function (directxmath.h)
description: Estimates the sine of each component of an XMVECTOR.helpviewer_keywords: ["Use DirectX..XMVectorSinEst","XMVectorSinEst","XMVectorSinEst method [DirectX Math Support APIs]","dxmath.xmvectorsinest"]
old-location: dxmath\xmvectorsinest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorSinEst(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSinEst, XMVectorSinEst, XMVectorSinEst method [DirectX Math Support APIs], dxmath.xmvectorsinest
f1_keywords:
- directxmath/XMVectorSinEst
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxmathvector.inl
api_name:
- XMVectorSinEst
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorSinEst function


## -description


Estimates the sine of each component of an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the sine.


## -returns



Returns a vector. Each component is an estimate of the sine of the corresponding component of <i>V</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses an 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorasin">XMVectorASin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorasinest">XMVectorASinEst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorsin">XMVectorSin</a>
 

 

