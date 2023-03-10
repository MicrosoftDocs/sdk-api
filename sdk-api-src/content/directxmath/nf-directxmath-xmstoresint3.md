---
UID: NF:directxmath.XMStoreSInt3
title: XMStoreSInt3 function (directxmath.h)
description: Stores signed integer data from an XMVECTOR in an XMINT3 structure.
helpviewer_keywords: ["Use DirectX..XMStoreSInt3","XMStoreSInt3","XMStoreSInt3 method [DirectX Math Support APIs]","dxmath.xmstoresint3"]
old-location: dxmath\xmstoresint3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreSInt3(XMINT3@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreSInt3, XMStoreSInt3, XMStoreSInt3 method [DirectX Math Support APIs], dxmath.xmstoresint3
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
 - XMStoreSInt3
 - directxmath/XMStoreSInt3
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
 - XMStoreSInt3
---

# XMStoreSInt3 function


## -description

Stores signed integer data from an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <b>XMINT3</b> structure.

## -parameters

### -param pDestination [out]

Address of an  <a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a> structure in which to store the data.

### -param V

Vector containing the data to store.

## -returns

None.

## -remarks

For 16-byte aligned memory, it may be faster to use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmstoreint3a">XMStoreInt3A</a> with a casting operator.

The following pseudocode shows the operation of this function.


```

XMVECTOR N;	

assert(pDestination);

N = XMVectorClamp(V, MinInt, MaxInt );
N = XMVectorRound(N);

pDestination->x = (int32_t)N.v[0];
pDestination->y = (int32_t)N.v[1];
pDestination->z = (int32_t)N.v[2];


    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>