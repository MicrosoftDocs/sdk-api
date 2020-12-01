---
UID: NF:directxmath.XMColorIsNaN
title: XMColorIsNaN function (directxmath.h)
description: Tests to see whether any component of a color is not a number (NaN).
helpviewer_keywords: ["Use DirectX..XMColorIsNaN","XMColorIsNaN","XMColorIsNaN method [DirectX Math Support APIs]","dxmath.xmcolorisnan"]
old-location: dxmath\xmcolorisnan.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorIsNaN(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorIsNaN, XMColorIsNaN, XMColorIsNaN method [DirectX Math Support APIs], dxmath.xmcolorisnan
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
 - XMColorIsNaN
 - directxmath/XMColorIsNaN
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
 - XMColorIsNaN
---

# XMColorIsNaN function


## -description

Tests to see whether any component of a color is not a number (NaN).

## -parameters

### -param C [in]

<b>XMVECTOR</b> describing the color.

## -returns

Returns true if any components of <i>C</i> are NaN, or false otherwise.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>