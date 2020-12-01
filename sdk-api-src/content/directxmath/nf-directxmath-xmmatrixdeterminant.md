---
UID: NF:directxmath.XMMatrixDeterminant
title: XMMatrixDeterminant function (directxmath.h)
description: Computes the determinant of a matrix.
helpviewer_keywords: ["Use DirectX..XMMatrixDeterminant","XMMatrixDeterminant","XMMatrixDeterminant method [DirectX Math Support APIs]","dxmath.xmmatrixdeterminant"]
old-location: dxmath\xmmatrixdeterminant.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixDeterminant(XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixDeterminant, XMMatrixDeterminant, XMMatrixDeterminant method [DirectX Math Support APIs], dxmath.xmmatrixdeterminant
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
 - XMMatrixDeterminant
 - directxmath/XMMatrixDeterminant
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
 - XMMatrixDeterminant
---

# XMMatrixDeterminant function


## -description

Computes the determinant of a matrix.

## -parameters

### -param M [in]

Matrix from which to compute the determinant.

## -returns

Returns a vector. The determinant of <i>M</i> is replicated into each component.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>