---
UID: NF:directxpackedvector.XMStoreColor
title: XMStoreColor function (directxpackedvector.h)
description: Stores an XMVECTOR in an XMCOLOR.
helpviewer_keywords: ["DirectX::PackedVector.XMStoreColor","XMStoreColor","XMStoreColor method [DirectX Math Support APIs]","dxmath.xmstorecolor"]
old-location: dxmath\xmstorecolor.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreColor(XMCOLOR@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMStoreColor, XMStoreColor, XMStoreColor method [DirectX Math Support APIs], dxmath.xmstorecolor
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
 - XMStoreColor
 - directxpackedvector/XMStoreColor
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
 - XMStoreColor
---

# XMStoreColor function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data.

### -param V [in]

Vector containing the data to store. X contains the Red color channel, Y contains the Green, Z the Blue, and W the Alpha
        channel.

## -returns

None.

## -remarks

The function takes a vector, clamps it to the range 0.0f to 1.0f, converts the components into a unsigned, normalized
   integer format, packs the components into a 32-bit integer, and writes the result out to the given address. The most
   significant component is written to the second most significant eight bits of the integer, and so on.

The following pseudocode demonstrates the operation of the function.


```
XMVector N;

N = saturate(V);
N = scale(N, 255.0f);
N = round(N);

pDestination->c = ((uint32_t)N.w << 24) |
                  ((uint32_t)N.x << 16) |
                  ((uint32_t)N.y << 8) |
                  ((uint32_t)N.z);
```


For Direct3D 10.x and Direct3D 11, this matches the component order for functions that take a float ColorRGBA[4] parameter.


```

 XMVECTOR Yellow = XMVectorSet( 1.0f, 1.0f, 0.0f, 1.0f );

 XMFLOAT4 clrf;
 XMStoreFloat4( &clrf, Yellow );
 pDeviceContext->ClearRenderTargetView( pRTV, (const float*)clrf );

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>