---
UID: NF:directxmath.XMStoreFloat3x3
title: XMStoreFloat3x3 function (directxmath.h)
description: Stores an XMMATRIX in an XMFLOAT3X3.
helpviewer_keywords: ["Use DirectX..XMStoreFloat3x3","XMStoreFloat3x3","XMStoreFloat3x3 method [DirectX Math Support APIs]","dxmath.xmstorefloat3x3"]
old-location: dxmath\xmstorefloat3x3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat3x3(XMFLOAT3X3@,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat3x3, XMStoreFloat3x3, XMStoreFloat3x3 method [DirectX Math Support APIs], dxmath.xmstorefloat3x3
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
 - XMStoreFloat3x3
 - directxmath/XMStoreFloat3x3
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
 - XMStoreFloat3x3
---

# XMStoreFloat3x3 function


## -description

Stores an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> in an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3x3">XMFLOAT3X3</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data.

### -param M [in]

Matrix containing the data to store.

## -returns

None.

## -remarks

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3x3">XMFLOAT3X3</a> is a row-major matrix form. To write out column-major data requires the XMMATRIX be 
    transposed via <a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrixtranspose">XMMatrixTranpose</a> before calling the store function.

This function takes a matrix and writes the components out to nine single-precision floating-point values at the given
    address. The most significant component of the first row vector is written to the first four bytes of the address,
    followed by the second most significant component of the first row, followed by the third most significant component
    of the first row. The most significant three components of the second row are then written out in a like manner to
    memory beginning at byte 12, followed by the third row to memory beginning at byte 24.

The following pseudocode demonstrates the operation of the function.


```
pDestination->_11 = M[0].x; // 4 bytes to address (uint8_t*)pDestination
pDestination->_12 = M[0].y; // 4 bytes to address (uint8_t*)pDestination + 4
pDestination->_13 = M[0].z; // 4 bytes to address (uint8_t*)pDestination + 8

pDestination->_21 = M[1].x; // 4 bytes to address (uint8_t*)pDestination + 12
pDestination->_22 = M[1].y; // 4 bytes to address (uint8_t*)pDestination + 16
pDestination->_23 = M[1].z; // 4 bytes to address (uint8_t*)pDestination + 20

pDestination->_31 = M[2].x; // 4 bytes to address (uint8_t*)pDestination + 24
pDestination->_32 = M[2].y; // 4 bytes to address (uint8_t*)pDestination + 28
pDestination->_33 = M[2].z; // 4 bytes to address (uint8_t*)pDestination + 32
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>