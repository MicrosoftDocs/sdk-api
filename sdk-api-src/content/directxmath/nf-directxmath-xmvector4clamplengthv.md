---
UID: NF:directxmath.XMVector4ClampLengthV
title: XMVector4ClampLengthV function (directxmath.h)
description: Clamps the length of a 4D vector to a given range. (XMVector4ClampLengthV)
helpviewer_keywords: ["Use DirectX..XMVector4ClampLengthV","XMVector4ClampLengthV","XMVector4ClampLengthV method [DirectX Math Support APIs]","dxmath.xmvector4clamplengthv"]
old-location: dxmath\xmvector4clamplengthv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4ClampLengthV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4ClampLengthV, XMVector4ClampLengthV, XMVector4ClampLengthV method [DirectX Math Support APIs], dxmath.xmvector4clamplengthv
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
 - XMVector4ClampLengthV
 - directxmath/XMVector4ClampLengthV
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
 - XMVector4ClampLengthV
---

# XMVector4ClampLengthV function


## -description

Clamps the length of a 4D vector to a given range.

## -parameters

### -param V [in]

4D vector to clamp.

### -param LengthMin [in]

4D vector, all of whose components are equal to the minimum clamp length. The components must be greater-than-or-equal to zero.

### -param LengthMax [in]

4D vector, all of whose components are equal to the maximum clamp length. The components must be greater-than-or-equal to zero.

## -returns

Returns a 4D vector whose length is clamped to the specified minimum and maximum.

## -remarks

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4clamplength">XMVector4ClampLength</a> except that <i>LengthMin</i> and <i>LengthMax</i> are supplied using 4D vectors instead of <b>float</b> values.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4clamplength">XMVector4ClampLength</a>
