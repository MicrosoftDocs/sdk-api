---
UID: NF:directxpackedvector.XMStoreFloat3PK
title: XMStoreFloat3PK function (directxpackedvector.h)
description: Stores an XMVECTOR in a XMFLOAT3PK.
helpviewer_keywords: ["DirectX::PackedVector.XMStoreFloat3PK","XMStoreFloat3PK","XMStoreFloat3PK method [DirectX Math Support APIs]","dxmath.xmstorefloat3pk"]
old-location: dxmath\xmstorefloat3pk.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat3PK(XMFLOAT3PK@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMStoreFloat3PK, XMStoreFloat3PK, XMStoreFloat3PK method [DirectX Math Support APIs], dxmath.xmstorefloat3pk
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
 - XMStoreFloat3PK
 - directxpackedvector/XMStoreFloat3PK
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
 - XMStoreFloat3PK
---

# XMStoreFloat3PK function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in a <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>.

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

  static const XMVECTOR  Max = { 65024.f, 65024.f, 64512.f, 0 };
  N = XMVectorClamp(V, XMVectorZero(), Max);

  ConvertToFloat11( N.x, &pDestination->xm, &pDestination->xe);
  ConvertToFloat11( N.y, &pDestination->ym, &pDestination->ye);
  ConvertToFloat10( N.z, &pDestination->zm, &pDesitnation->ze);

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>