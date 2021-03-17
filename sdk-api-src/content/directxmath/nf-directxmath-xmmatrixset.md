---
UID: NF:directxmath.XMMatrixSet
title: XMMatrixSet function (directxmath.h)
description: Creates a matrix with float values.
helpviewer_keywords: ["Use DirectX..XMMatrixSet","XMMatrixSet","XMMatrixSet method [DirectX Math Support APIs]","dxmath.xmmatrixset"]
old-location: dxmath\xmmatrixset.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixSet(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixSet, XMMatrixSet, XMMatrixSet method [DirectX Math Support APIs], dxmath.xmmatrixset
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
 - XMMatrixSet
 - directxmath/XMMatrixSet
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
 - XMMatrixSet
---

# XMMatrixSet function


## -description

Creates a matrix with <b>float</b> values.

## -parameters

### -param m00 [in]

Value to assign to the (0,0) element.

### -param m01 [in]

Value to assign to the (0,1) element.

### -param m02 [in]

Value to assign to the (0,2) element.

### -param m03 [in]

Value to assign to the (0,3) element.

### -param m10 [in]

Value to assign to the (1,0) element.

### -param m11 [in]

Value to assign to the (1,1) element.

### -param m12 [in]

Value to assign to the (1,2) element.

### -param m13 [in]

Value to assign to the (1,3) element.

### -param m20 [in]

Value to assign to the (2,0) element.

### -param m21 [in]

Value to assign to the (2,1) element.

### -param m22 [in]

Value to assign to the (2,2) element.

### -param m23 [in]

Value to assign to the (2,3) element.

### -param m30 [in]

Value to assign to the (3,0) element.

### -param m31 [in]

Value to assign to the (3,1) element.

### -param m32 [in]

Value to assign to the (3,2) element.

### -param m33 [in]

Value to assign to the (3,3) element.

## -returns

Returns the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> with the specified elements.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>