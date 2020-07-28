---
UID: NF:directxmath.XMStoreInt
title: XMStoreInt function (directxmath.h)
description: Stores an XMVECTOR in a uint32_t.
helpviewer_keywords: ["Use DirectX..XMStoreInt","XMStoreInt","XMStoreInt method [DirectX Math Support APIs]","dxmath.xmstoreint"]
old-location: dxmath\xmstoreint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreInt(uint32_t@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreInt, XMStoreInt, XMStoreInt method [DirectX Math Support APIs], dxmath.xmstoreint
f1_keywords:
- directxmath/XMStoreInt
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
- XMStoreInt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMStoreInt function


## -description


Stores an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in a <b>uint32_t</b>.


## -parameters




### -param pDestination [out]

Address at which to store the data. The data pointed to by this parameter must be 4-byte aligned and reside in cached
        memory.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



The following pseudocode demonstrates the operation of the function.


```
uint32_t* pElement = (uint32_t*)pDestination;

assert(pDestination);
assert(((uint32_t_PTR)pDestination & 3) == 0);

*pElement = V.u[0];
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>
 

 

