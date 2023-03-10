---
UID: NF:directxmath.XMLoadFloat4x4A
title: XMLoadFloat4x4A function (directxmath.h)
description: Loads an XMFLOAT4X4A into an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadFloat4x4A","XMLoadFloat4x4A","XMLoadFloat4x4A method [DirectX Math Support APIs]","dxmath.xmloadfloat4x4a"]
old-location: dxmath\xmloadfloat4x4a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat4x4A(const XMFLOAT4X4A)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadFloat4x4A, XMLoadFloat4x4A, XMLoadFloat4x4A method [DirectX Math Support APIs], dxmath.xmloadfloat4x4a
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
 - XMLoadFloat4x4A
 - directxmath/XMLoadFloat4x4A
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
 - XMLoadFloat4x4A
---

# XMLoadFloat4x4A function


## -description

Loads an <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

<a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> is a row-major form of the matrix. This function could be used to read column-major data, 
    but would then need to be transposed with <a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrixtranspose">XMMatrixTranpose</a> before use in other XMMATRIX functions.

The members of the <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> structure (<b>_11</b>, <b>_12</b>,
   <b>_13</b>, and so on) are loaded into the corresponding members of the
   <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>