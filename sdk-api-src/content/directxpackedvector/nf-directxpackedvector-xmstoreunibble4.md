---
UID: NF:directxpackedvector.XMStoreUNibble4
title: XMStoreUNibble4 function (directxpackedvector.h)
description: Stores an XMVECTOR in an XMUNIBBLE4.
helpviewer_keywords: ["DirectX::PackedVector.XMStoreUNibble4","XMStoreUNibble4","XMStoreUNibble4 method [DirectX Math Support APIs]","dxmath.xmstoreunibble4"]
old-location: dxmath\xmstoreunibble4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreUNibble4(XMUNIBBLE4@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMStoreUNibble4, XMStoreUNibble4, XMStoreUNibble4 method [DirectX Math Support APIs], dxmath.xmstoreunibble4
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
 - XMStoreUNibble4
 - directxpackedvector/XMStoreUNibble4
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
 - XMStoreUNibble4
---

# XMStoreUNibble4 function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>.

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
  static const XMVECTOR  Max = {15.f, 15.f, 15.f, 15.f };

  N = XMVectorClamp(V, XMVectorZero, Max);
  N = XMVectorRound(N);

  pDestination->x = (int8_t)N.v[0];
  pDestination->y = (int8_t)N.v[1];
  pDestination->z = (int8_t)N.v[2];
  pDestination->w = (int8_t)N.v[3];


```


Note these are not normalized values. To convert to the RGBA 4/4/4/4 format, 
    you must scale the input vector by <code>(15.f, 15.f, 15.f, 15.f)</code>. 
    Also, you will probably need to swizzle 
    the standard .x = RED, .y = GREEN, .z = BLUE, .w = ALPHA color vector's .x and .z value 
    since the GPU format is BGR (not RGB).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>