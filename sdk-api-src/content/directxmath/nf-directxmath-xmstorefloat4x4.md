---
UID: NF:directxmath.XMStoreFloat4x4
title: XMStoreFloat4x4 function (directxmath.h)
description: Stores an XMMATRIX in an XMFLOAT4X4.
helpviewer_keywords: ["Use DirectX..XMStoreFloat4x4","XMStoreFloat4x4","XMStoreFloat4x4 method [DirectX Math Support APIs]","dxmath.xmstorefloat4x4"]
old-location: dxmath\xmstorefloat4x4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat4x4(XMFLOAT4X4@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat4x4, XMStoreFloat4x4, XMStoreFloat4x4 method [DirectX Math Support APIs], dxmath.xmstorefloat4x4
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
 - XMStoreFloat4x4
 - directxmath/XMStoreFloat4x4
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
 - XMStoreFloat4x4
---

# XMStoreFloat4x4 function


## -description

Stores an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> in an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data.

### -param M [in]

Matrix containing the data to store.

## -returns

None.

## -remarks

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a> is a row-major matrix form. To write out column-major data requires the 
    XMMATRIX be transposed via <a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrixtranspose">XMMatrixTranpose</a> before calling the store function.

This function takes a matrix and writes the components out to sixteen single-precision floating-point values at the
    given address. The most significant component of the first row vector is written to the first four bytes of the
    address, followed by the second most significant component of the first row, and so on. The second row is then
    written out in a like manner to memory beginning at byte 16, followed by the third row to memory beginning at byte
    32, and finally the fourth row to memory beginning at byte 48.

The following pseudocode demonstrates the operation of the function.


```
pDestination->_11 = M[0].x; // 4 bytes to address (uint8_t*)pDestination
pDestination->_12 = M[0].y; // 4 bytes to address (uint8_t*)pDestination + 4
pDestination->_13 = M[0].z; // 4 bytes to address (uint8_t*)pDestination + 8
pDestination->_14 = M[0].w; // 4 bytes to address (uint8_t*)pDestination + 12

pDestination->_21 = M[1].x; // 4 bytes to address (uint8_t*)pDestination + 16
pDestination->_22 = M[1].y; // 4 bytes to address (uint8_t*)pDestination + 20
pDestination->_23 = M[1].z; // 4 bytes to address (uint8_t*)pDestination + 24
pDestination->_24 = M[1].w; // 4 bytes to address (uint8_t*)pDestination + 28

pDestination->_31 = M[2].x; // 4 bytes to address (uint8_t*)pDestination + 32
pDestination->_32 = M[2].y; // 4 bytes to address (uint8_t*)pDestination + 36
pDestination->_33 = M[2].z; // 4 bytes to address (uint8_t*)pDestination + 40
pDestination->_34 = M[2].w; // 4 bytes to address (uint8_t*)pDestination + 44

pDestination->_41 = M[3].x; // 4 bytes to address (uint8_t*)pDestination + 48
pDestination->_42 = M[3].y; // 4 bytes to address (uint8_t*)pDestination + 52
pDestination->_43 = M[3].z; // 4 bytes to address (uint8_t*)pDestination + 56
pDestination->_44 = M[3].w; // 4 bytes to address (uint8_t*)pDestination + 60
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>