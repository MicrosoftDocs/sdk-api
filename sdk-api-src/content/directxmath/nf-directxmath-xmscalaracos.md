---
UID: NF:directxmath.XMScalarACos
title: XMScalarACos function (directxmath.h)
description: Computes the arccosine of a floating-point number.
helpviewer_keywords: ["Use DirectX..XMScalarACos","XMScalarACos","XMScalarACos method [DirectX Math Support APIs]","dxmath.xmscalaracos"]
old-location: dxmath\xmscalaracos.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarACos(float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMScalarACos, XMScalarACos, XMScalarACos method [DirectX Math Support APIs], dxmath.xmscalaracos
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
 - XMScalarACos
 - directxmath/XMScalarACos
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
 - XMScalarACos
---

# XMScalarACos function


## -description

Computes the arccosine of a floating-point number.

## -parameters

### -param Value [in]

<b>float</b> value between -1.0f and 1.0f.

## -returns

Returns the inverse cosine of <i>Value</i>.

## -remarks

This function uses a 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-scalar">DirectXMath Library Scalar Functions</a>



<a href="/windows/win32/api/directxmath/nf-directxmath-xmscalaracosest">XMScalarACosEst</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmscalarcos">XMScalarCos</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmscalarcosest">XMScalarCosEst</a>
