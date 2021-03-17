---
UID: NF:directxmath.XMStoreInt3
title: XMStoreInt3 function (directxmath.h)
description: Stores an XMVECTOR in a 3-element uint32_t array.
helpviewer_keywords: ["Use DirectX..XMStoreInt3","XMStoreInt3","XMStoreInt3 method [DirectX Math Support APIs]","dxmath.xmstoreint3"]
old-location: dxmath\xmstoreint3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreInt3(VOID@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreInt3, XMStoreInt3, XMStoreInt3 method [DirectX Math Support APIs], dxmath.xmstoreint3
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
 - XMStoreInt3
 - directxmath/XMStoreInt3
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
 - XMStoreInt3
---

# XMStoreInt3 function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in a 3-element <b>uint32_t</b> array.

## -parameters

### -param pDestination [out]

Address at which to store the data. This pointer must be 4-byte aligned.

### -param V [in]

Vector containing the data to store.

## -returns

None.

## -remarks

The following pseudocode shows you the operation of the function.


```
uint32_t* pElement = (uint32_t*)pDestination;

assert(pDestination);
assert(((uint32_t_PTR)pDestination & 3) == 0);

pElement[0] = V.u[0];
pElement[1] = V.u[1];
pElement[2] = V.u[2];
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmstoresint3">XMStoreSInt3</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmstoreuint3">XMStoreUInt3</a>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint3">XMUINT3</a>