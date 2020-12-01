---
UID: NF:directxmath.XMMatrixInverse
title: XMMatrixInverse function (directxmath.h)
description: Computes the inverse of a matrix.
helpviewer_keywords: ["Use DirectX..XMMatrixInverse","XMMatrixInverse","XMMatrixInverse method [DirectX Math Support APIs]","dxmath.xmmatrixinverse"]
old-location: dxmath\xmmatrixinverse.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixInverse(XMVECTOR@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixInverse, XMMatrixInverse, XMMatrixInverse method [DirectX Math Support APIs], dxmath.xmmatrixinverse
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
 - XMMatrixInverse
 - directxmath/XMMatrixInverse
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
 - XMMatrixInverse
---

# XMMatrixInverse function


## -description

Computes the inverse of a matrix.

## -parameters

### -param pDeterminant [out, optional]

Address of a vector, each of whose components receives the determinant of <i>M</i>. This parameter can be nullptr if the determinant is not desired.

### -param M [in]

Matrix to invert.

## -returns

Returns the matrix inverse of <i>M</i>. If there is no inverse (that is, if the determinant is 0),
       <b>XMMatrixInverse</b> returns an infinite matrix.

## -remarks

<div class="alert"><b>Note</b>  For XNAMATH version 2.04 and earlier, the <i>pDeterminant</i> parameter isn't optional. That is, for XNAMATH version 2.04 and earlier, you can't set <i>pDeterminant</i> to a nullptr.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>