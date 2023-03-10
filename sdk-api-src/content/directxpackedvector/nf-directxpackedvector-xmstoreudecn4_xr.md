---
UID: NF:directxpackedvector.XMStoreUDecN4_XR
title: XMStoreUDecN4_XR function (directxpackedvector.h)
description: Stores an extended range XMUDECN4 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMStoreUDecN4_XR","XMStoreUDecN4_XR","XMStoreUDecN4_XR method [DirectX Math Support APIs]","dxmath._xmstoreudecn4_xr"]
old-location: dxmath\_xmstoreudecn4_xr.htm
tech.root: dxmath
ms.assetid: 4DCE74D6-48CF-43D8-BF69-368A95F823F1
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMStoreUDecN4_XR, XMStoreUDecN4_XR, XMStoreUDecN4_XR method [DirectX Math Support APIs], dxmath._xmstoreudecn4_xr
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: DirectX::PackedVector
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
 - XMStoreUDecN4_XR
 - directxpackedvector/XMStoreUDecN4_XR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxpackedvector.inl
api_name:
 - XMStoreUDecN4_XR
---

# XMStoreUDecN4_XR function


## -description

Stores an extended range <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. This type stores a 10:10:10:2 normalized GPU format using the Extended Range (XR) with the color bias set to match DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM.

## -parameters

### -param pDestination [out]

Address at which to store the data.

### -param V [in]

Vector containing the data to store.

## -returns

None.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR N; 
static const XMVECTOR Scale = {510.0f, 510.0f, 510.0f, 3.0f};
static const XMVECTOR Bias = { 384.0f, 384.0f, 384.0f, 0.0f };
static const XMVECTOR C = { 1023.f, 1023.f, 1023.f, 3.f };

assert(pDestination);

N = XMVectorMultiplyAdd( V, Scale, Bias );
N = XMVectorClamp( V, XMVectorZero(), C );

pDestination->v = ((uint32_t)N.v[3] << 30) |
(((uint32_t)N.v[2] & 0x3FF) << 20) |
(((uint32_t)N.v[1] & 0x3FF) << 10) |
(((uint32_t)N.v[0] & 0x3FF));
```


For more details on the Extended Range (XR) with Bias conversion, see <a href="/windows-hardware/drivers/display/xr-bias-color-channel-conversion-rules">XR_BIAS Color Channel Conversion Rules</a>. 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>



<a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr">XMLoadUDecN4_XR</a>