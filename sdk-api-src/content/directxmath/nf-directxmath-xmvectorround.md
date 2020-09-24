---
UID: NF:directxmath.XMVectorRound
title: XMVectorRound function (directxmath.h)
description: Rounds each component of a vector to the nearest even integer (known as &quot;Bankers Rounding&quot;).
helpviewer_keywords: ["Use DirectX..XMVectorRound","XMVectorRound","XMVectorRound method [DirectX Math Support APIs]","dxmath.xmvectorround"]
old-location: dxmath\xmvectorround.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorRound(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorRound, XMVectorRound, XMVectorRound method [DirectX Math Support APIs], dxmath.xmvectorround
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
 - XMVectorRound
 - directxmath/XMVectorRound
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
 - XMVectorRound
---

# XMVectorRound function


## -description

Rounds each component of a vector to the nearest even integer (known as "Bankers Rounding").

## -parameters

### -param V [in]

Vector whose components should be rounded.

## -returns

Returns a vector, each of whose components are rounded to the nearest integer.

## -remarks

Banker's Rounding is used because it is the native vector rounding intrinsic method for both SSE4 and ARMv8 NEON.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>