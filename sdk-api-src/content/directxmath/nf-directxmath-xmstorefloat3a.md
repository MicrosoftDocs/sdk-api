---
UID: NF:directxmath.XMStoreFloat3A
title: XMStoreFloat3A function (directxmath.h)
description: Stores an XMVECTOR in an XMFLOAT3A.
helpviewer_keywords: ["Use DirectX..XMStoreFloat3A","XMStoreFloat3A","XMStoreFloat3A method [DirectX Math Support APIs]","dxmath.xmstorefloat3a"]
old-location: dxmath\xmstorefloat3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat3A(XMFLOAT3A@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat3A, XMStoreFloat3A, XMStoreFloat3A method [DirectX Math Support APIs], dxmath.xmstorefloat3a
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
 - XMStoreFloat3A
 - directxmath/XMStoreFloat3A
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
 - XMStoreFloat3A
---

# XMStoreFloat3A function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3a">XMFLOAT3A</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data. This address must be 16-byte aligned.

### -param V [in]

Vector containing the data to store.

## -returns

None.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
return (XMFLOAT3A*)XMStoreVector3A(pDestination, V);
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>