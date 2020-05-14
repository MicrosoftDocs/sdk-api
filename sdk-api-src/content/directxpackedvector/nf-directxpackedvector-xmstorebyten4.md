---
UID: NF:directxpackedvector.XMStoreByteN4
title: XMStoreByteN4 function (directxpackedvector.h)
description: Stores an XMVECTOR in an XMBYTEN4.helpviewer_keywords: ["DirectX::PackedVector.XMStoreByteN4","XMStoreByteN4","XMStoreByteN4 method [DirectX Math Support APIs]","dxmath.xmstorebyten4"]
old-location: dxmath\xmstorebyten4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreByteN4(XMBYTEN4@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMStoreByteN4, XMStoreByteN4, XMStoreByteN4 method [DirectX Math Support APIs], dxmath.xmstorebyten4
f1_keywords:
- directxpackedvector/XMStoreByteN4
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxpackedvector.inl
api_name:
- XMStoreByteN4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMStoreByteN4 function


## -description


Stores an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>.


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
static const XMVECTOR  Scale = {127.0f, 127.0f, 127.0f, 127.0f};

N = XMVectorMultiply(V, Scale);
N = XMVectorRound(N);

pDestination->x = (int8_t)N.v[0];
pDestination->y = (int8_t)N.v[1];
pDestination->z = (int8_t)N.v[2];
pDestination->w = (int8_t)N.v[3];
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>
 

 

