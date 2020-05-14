---
UID: NF:directxmath.XMStoreFloat2
title: XMStoreFloat2 function (directxmath.h)
description: Stores an XMVECTOR in an XMFLOAT2.helpviewer_keywords: ["Use DirectX..XMStoreFloat2","XMStoreFloat2","XMStoreFloat2 method [DirectX Math Support APIs]","dxmath.xmstorefloat2"]
old-location: dxmath\xmstorefloat2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat2(XMFLOAT2@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat2, XMStoreFloat2, XMStoreFloat2 method [DirectX Math Support APIs], dxmath.xmstorefloat2
f1_keywords:
- directxmath/XMStoreFloat2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXMath.h
api_name:
- XMStoreFloat2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMStoreFloat2 function


## -description


Stores an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a>.


## -parameters




### -param pDestination [out]

Address at which to store the data.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



This function takes a vector and writes the two most significant components out to two single-precision floating-point values at the given address. The most significant component is written to the first four bytes of the address, and the next most significant component is written to the next four bytes of the address.

The following pseudocode demonstrates the operation of the function.


```
pDestination->x = V.x; // 4 bytes to address pDestination
pDestination->y = V.y; // 4 bytes to address (uint8_t*)pDestination + 4
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>
 

 

