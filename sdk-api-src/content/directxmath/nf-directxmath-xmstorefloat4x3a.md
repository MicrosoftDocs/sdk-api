---
UID: NF:directxmath.XMStoreFloat4x3A
title: XMStoreFloat4x3A function (directxmath.h)
description: Stores an XMVECTOR in an XMFLOAT4X3A.
helpviewer_keywords: ["Use DirectX..XMStoreFloat4x3A","XMStoreFloat4x3A","XMStoreFloat4x3A method [DirectX Math Support APIs]","dxmath.xmstorefloat4x3a"]
old-location: dxmath\xmstorefloat4x3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat4x3A(XMFLOAT4X3A@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat4x3A, XMStoreFloat4x3A, XMStoreFloat4x3A method [DirectX Math Support APIs], dxmath.xmstorefloat4x3a
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
 - XMStoreFloat4x3A
 - directxmath/XMStoreFloat4x3A
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
 - XMStoreFloat4x3A
---

# XMStoreFloat4x3A function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/previous-versions/windows/desktop/legacy/ee419612(v=vs.85)">XMFLOAT4X3A</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data. This address must be 16-byte aligned.

### -param M [in]

Matrix containing the data to store.

## -returns

None.

## -remarks

<a href="/previous-versions/windows/desktop/legacy/ee419612(v=vs.85)">XMFLOAT4X3A</a> is a row-major matrix form. This function cannot be used 
   to write out column-major data since it assumes the last column is 


```
assert(pDestination);
assert(((uint32_t_PTR)pDestination & 0xF) == 0);

pDestination->m[0][0] = M.r[0].v[0];
pDestination->m[0][1] = M.r[0].v[1];
pDestination->m[0][2] = M.r[0].v[2];

pDestination->m[1][0] = M.r[1].v[0];
pDestination->m[1][1] = M.r[1].v[1];
pDestination->m[1][2] = M.r[1].v[2];

pDestination->m[2][0] = M.r[2].v[0];
pDestination->m[2][1] = M.r[2].v[1];
pDestination->m[2][2] = M.r[2].v[2];

pDestination->m[3][0] = M.r[3].v[0];
pDestination->m[3][1] = M.r[3].v[1];
pDestination->m[3][2] = M.r[3].v[2];
```

.

The following pseudocode demonstrates the operation of the function.

<code>0 0 0 1</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>