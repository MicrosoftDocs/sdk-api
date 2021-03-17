---
UID: NF:directxmath.XMMatrixIsInfinite
title: XMMatrixIsInfinite function (directxmath.h)
description: Tests whether any of the elements of a matrix are positive or negative infinity.
helpviewer_keywords: ["Use DirectX..XMMatrixIsInfinite","XMMatrixIsInfinite","XMMatrixIsInfinite method [DirectX Math Support APIs]","dxmath.xmmatrixisinfinite"]
old-location: dxmath\xmmatrixisinfinite.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixIsInfinite(XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixIsInfinite, XMMatrixIsInfinite, XMMatrixIsInfinite method [DirectX Math Support APIs], dxmath.xmmatrixisinfinite
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
 - XMMatrixIsInfinite
 - directxmath/XMMatrixIsInfinite
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
 - XMMatrixIsInfinite
---

# XMMatrixIsInfinite function


## -description

Tests whether any of the elements of a matrix are positive or negative infinity.

## -parameters

### -param M [in]

Matrix to test.

## -returns

Returns true if any element of <i>M</i> is either positive or negative infinity, and false otherwise.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>