---
UID: NF:directxmath.XMColorIsInfinite
title: XMColorIsInfinite function (directxmath.h)
description: Tests to see whether any of the components of a color are either positive or negative infinity.
helpviewer_keywords: ["Use DirectX..XMColorIsInfinite","XMColorIsInfinite","XMColorIsInfinite method [DirectX Math Support APIs]","dxmath.xmcolorisinfinite"]
old-location: dxmath\xmcolorisinfinite.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorIsInfinite(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorIsInfinite, XMColorIsInfinite, XMColorIsInfinite method [DirectX Math Support APIs], dxmath.xmcolorisinfinite
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
 - XMColorIsInfinite
 - directxmath/XMColorIsInfinite
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
 - XMColorIsInfinite
---

# XMColorIsInfinite function


## -description

Tests to see whether any of the components of a color are either positive or negative infinity.

## -parameters

### -param C [in]

<b>XMVECTOR</b> describing the color.

## -returns

Returns true if any components of <i>C</i> are either positive or negative infinity. Returns false otherwise.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>