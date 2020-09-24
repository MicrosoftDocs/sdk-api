---
UID: NF:directxmath.XMMatrixDecompose
title: XMMatrixDecompose function (directxmath.h)
description: Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.
helpviewer_keywords: ["Use DirectX..XMMatrixDecompose","XMMatrixDecompose","XMMatrixDecompose method [DirectX Math Support APIs]","dxmath.xmmatrixdecompose"]
old-location: dxmath\xmmatrixdecompose.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixDecompose(XMVECTOR@,XMVECTOR@,XMVECTOR@,XMMATRIX )
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixDecompose, XMMatrixDecompose, XMMatrixDecompose method [DirectX Math Support APIs], dxmath.xmmatrixdecompose
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
 - XMMatrixDecompose
 - directxmath/XMMatrixDecompose
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
 - XMMatrixDecompose
---

# XMMatrixDecompose function


## -description

Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.

## -parameters

### -param outScale [in, out]

Pointer to the output <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> that contains scaling factors applied along the
        x, y, and z-axes.

### -param outRotQuat [in, out]

Pointer to the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> quaternion that describes the rotation.

### -param outTrans [in, out]

Pointer to the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> vector that describes a translation along the
        x, y, and z-axes.

### -param M [in]

Pointer to an input <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> matrix to decompose.

## -returns

If the function succeeds, the return value is true. If the function fails, the return value is false.

## -remarks

<b>XMMatrixDecompose</b> provides the same basic functionality found in both <a href="/windows/desktop/direct3d9/d3dxmatrixdecompose">D3DXMatrixDecompose (Direct3D 9)</a> and <a href="/windows/desktop/direct3d10/d3d10-d3dxmatrixdecompose">D3DXMatrixDecompose (Direct3D 10)</a>.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>