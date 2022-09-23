---
UID: NF:directxmath.XMStoreFloat4x4A
title: XMStoreFloat4x4A function (directxmath.h)
description: Stores an XMVECTOR in an XMFLOAT4X4A.
helpviewer_keywords: ["Use DirectX..XMStoreFloat4x4A","XMStoreFloat4x4A","XMStoreFloat4x4A method [DirectX Math Support APIs]","dxmath.xmstorefloat4x4a"]
old-location: dxmath\xmstorefloat4x4a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat4x4A(XMFLOAT4X4A@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat4x4A, XMStoreFloat4x4A, XMStoreFloat4x4A method [DirectX Math Support APIs], dxmath.xmstorefloat4x4a
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
 - XMStoreFloat4x4A
 - directxmath/XMStoreFloat4x4A
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
 - XMStoreFloat4x4A
---

# XMStoreFloat4x4A function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data. This address must be 16-byte aligned.

### -param M [in]

Matrix containing the data to store.

## -returns

None.

## -remarks

<a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4a">XMFLOAT4X4A</a> is a row-major matrix form. To write out column-major data requires the XMMATRIX be transposed 
   via <a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrixtranspose">XMMatrixTranpose</a> before calling the store function.

The following pseudocode demonstrates the operation of the function.


```
assert(pDestination);
assert(((uint32_t_PTR)pDestination & 0xF) == 0);

pDestination->m[0][0] = M.r[0].v[0];
pDestination->m[0][1] = M.r[0].v[1];
pDestination->m[0][2] = M.r[0].v[2];
pDestination->m[0][3] = M.r[0].v[3];

pDestination->m[1][0] = M.r[1].v[0];
pDestination->m[1][1] = M.r[1].v[1];
pDestination->m[1][2] = M.r[1].v[2];
pDestination->m[1][3] = M.r[1].v[3];

pDestination->m[2][0] = M.r[2].v[0];
pDestination->m[2][1] = M.r[2].v[1];
pDestination->m[2][2] = M.r[2].v[2];
pDestination->m[2][3] = M.r[2].v[3];

pDestination->m[3][0] = M.r[3].v[0];
pDestination->m[3][1] = M.r[3].v[1];
pDestination->m[3][2] = M.r[3].v[2];
pDestination->m[3][3] = M.r[3].v[3];
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>