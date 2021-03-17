---
UID: NF:directxmath.XMVector4GreaterOrEqualR
title: XMVector4GreaterOrEqualR function (directxmath.h)
description: Tests whether one 4D vector is greater-than-or-equal-to another 4D vector and returns a comparison value that can be examined using functions such as XMComparisonAllTrue.
helpviewer_keywords: ["Use DirectX..XMVector4GreaterOrEqualR","XMVector4GreaterOrEqualR","XMVector4GreaterOrEqualR method [DirectX Math Support APIs]","dxmath.xmvector4greaterorequalr"]
old-location: dxmath\xmvector4greaterorequalr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector4GreaterOrEqualR(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4GreaterOrEqualR, XMVector4GreaterOrEqualR, XMVector4GreaterOrEqualR method [DirectX Math Support APIs], dxmath.xmvector4greaterorequalr
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
 - XMVector4GreaterOrEqualR
 - directxmath/XMVector4GreaterOrEqualR
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
 - XMVector4GreaterOrEqualR
---

# XMVector4GreaterOrEqualR function


## -description

Tests whether one 4D vector is greater-than-or-equal-to another 4D vector and returns a comparison value that can be examined using functions such as <a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonalltrue">XMComparisonAllTrue</a>.

## -parameters

### -param V1 [in]

4D vector.

### -param V2 [in]

4D vector.

## -returns

Returns a comparison value that can be examined using functions such as <a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonalltrue">XMComparisonAllTrue</a>.

## -remarks

This function does the following test:


```
V1.x >= V2.x
V1.y >= V2.y
V1.z >= V2.z
V1.w >= V2.w
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-comparison">DirectXMath Library 4D Vector Comparison Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4greaterorequal">XMVector4GreaterOrEqual</a>