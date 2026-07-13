---
UID: NF:directxmath.XMLoadFloat4x3A
title: XMLoadFloat4x3A function (directxmath.h)
description: Loads an XMFLOAT4X3A into an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadFloat4x3A","XMLoadFloat4x3A","XMLoadFloat4x3A method [DirectX Math Support APIs]","dxmath.xmloadfloat4x3a"]
old-location: dxmath\xmloadfloat4x3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat4x3A(const XMFLOAT4X3A)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadFloat4x3A, XMLoadFloat4x3A, XMLoadFloat4x3A method [DirectX Math Support APIs], dxmath.xmloadfloat4x3a
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
 - XMLoadFloat4x3A
 - directxmath/XMLoadFloat4x3A
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
 - XMLoadFloat4x3A
---

# XMLoadFloat4x3A function


## -description

Loads an <a href="/previous-versions/windows/desktop/legacy/ee419612(v=vs.85)">XMFLOAT4X3A</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/previous-versions/windows/desktop/legacy/ee419612(v=vs.85)">XMFLOAT4X3A</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> loaded with the data from the <i>pSource</i> parameter.

This function performs a partial load of the returned <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>. See <a href="/windows/desktop/dxmath/pg-xnamath-getting-started">Getting Started</a> for more information.

## -remarks

<a href="/previous-versions/windows/desktop/legacy/ee419612(v=vs.85)">XMFLOAT4X3A</a> is a row-major form of the matrix. This function cannot be used to read column-major data since it assumes the last column is 0 0 0 1.

The members of the <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> structure (<b>_11</b>, <b>_12</b>,
   <b>_13</b>, and so on) are loaded into the corresponding members of the
   <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>. The remaining members of the returned
   <b>XMMATRIX</b> are 0.0f, except for <b>_44</b>, which is 1.0f.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>