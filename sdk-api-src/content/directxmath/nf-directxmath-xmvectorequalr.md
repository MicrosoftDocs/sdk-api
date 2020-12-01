---
UID: NF:directxmath.XMVectorEqualR
title: XMVectorEqualR function (directxmath.h)
description: Performs a per-component test for equality of two vectors and sets a comparison value that can be examined using functions such as XMComparisonAllTrue.
helpviewer_keywords: ["Use DirectX..XMVectorEqualR","XMVectorEqualR","XMVectorEqualR method [DirectX Math Support APIs]","dxmath.xmvectorequalr"]
old-location: dxmath\xmvectorequalr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorEqualR(uint32_t@,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorEqualR, XMVectorEqualR, XMVectorEqualR method [DirectX Math Support APIs], dxmath.xmvectorequalr
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
 - XMVectorEqualR
 - directxmath/XMVectorEqualR
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
 - XMVectorEqualR
---

# XMVectorEqualR function


## -description

Performs a per-component test for equality of two vectors and sets a comparison value that can be examined using functions such as <a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonalltrue">XMComparisonAllTrue</a>.

## -parameters

### -param pCR [out]

Pointer to a <b>uint32_t</b> comparison value that can be examined using functions such as <a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonalltrue">XMComparisonAllTrue</a>. The <code>XMComparisonXXXX</code> functions may be used to further test the number of components that passed the comparison.

### -param V1 [in]

First vector to compare.

### -param V2 [in]

Second vector to compare.

## -returns

Returns a vector containing the results of each component test.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-comparison">Vector Comparison Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorequal">XMVectorEqual</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorequalint">XMVectorEqualInt</a>