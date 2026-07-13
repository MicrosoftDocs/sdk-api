---
UID: NF:directxmath.XMVector2ClampLengthV
title: XMVector2ClampLengthV function (directxmath.h)
description: Clamps the length of a 2D vector to a given range. (XMVector2ClampLengthV)
helpviewer_keywords: ["Use DirectX..XMVector2ClampLengthV","XMVector2ClampLengthV","XMVector2ClampLengthV method [DirectX Math Support APIs]","dxmath.xmvector2clamplengthv"]
old-location: dxmath\xmvector2clamplengthv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2ClampLengthV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2ClampLengthV, XMVector2ClampLengthV, XMVector2ClampLengthV method [DirectX Math Support APIs], dxmath.xmvector2clamplengthv
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
 - XMVector2ClampLengthV
 - directxmath/XMVector2ClampLengthV
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
 - XMVector2ClampLengthV
---

# XMVector2ClampLengthV function


## -description

Clamps the length of a 2D vector to a given range.

## -parameters

### -param V [in]

2D vector to clamp.

### -param LengthMin [in]

2D vector whose x and y-components are both equal to the minimum clamp length. The x and y-components must be greater-than-or-equal to zero.

### -param LengthMax [in]

2D vector whose x and y-components are both equal to the maximum clamp length. The x and y-components must be greater-than-or-equal to zero.

## -returns

Returns a 2D vector whose length is clamped to the specified minimum and maximum.

## -remarks

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2clamplength">XMVector2ClampLength</a> except that <i>LengthMin</i> and <i>LengthMax</i> are supplied using 2D vectors instead of <b>float</b> values.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-geometric">DirectXMath Library 2D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2clamplength">XMVector2ClampLength</a>
