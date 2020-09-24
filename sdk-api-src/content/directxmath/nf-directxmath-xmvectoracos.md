---
UID: NF:directxmath.XMVectorACos
title: XMVectorACos function (directxmath.h)
description: Computes the arccosine of each component of an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMVectorACos","XMVectorACos","XMVectorACos method [DirectX Math Support APIs]","dxmath.xmvectoracos"]
old-location: dxmath\xmvectoracos.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorACos(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorACos, XMVectorACos, XMVectorACos method [DirectX Math Support APIs], dxmath.xmvectoracos
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
 - XMVectorACos
 - directxmath/XMVectorACos
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
 - XMVectorACos
---

# XMVectorACos function


## -description

Computes the arccosine of each component of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param V [in]

Vector for which to compute the arccosine. Each component should be between -1.0f and 1.0f.

## -returns

Returns a vector whose components are the arccosine of the corresponding components of <i>V</i>.

## -remarks

This function uses a 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectoracosest">XMVectorACosEst</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorcos">XMVectorCos</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorcosest">XMVectorCosEst</a>