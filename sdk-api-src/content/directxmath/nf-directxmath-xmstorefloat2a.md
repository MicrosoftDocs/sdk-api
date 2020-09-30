---
UID: NF:directxmath.XMStoreFloat2A
title: XMStoreFloat2A function (directxmath.h)
description: Stores an XMVECTOR in an XMFLOAT2A.
helpviewer_keywords: ["Use DirectX..XMStoreFloat2A","XMStoreFloat2A","XMStoreFloat2A method [DirectX Math Support APIs]","dxmath.xmstorefloat2a"]
old-location: dxmath\xmstorefloat2a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat2A(XMFLOAT2A@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreFloat2A, XMStoreFloat2A, XMStoreFloat2A method [DirectX Math Support APIs], dxmath.xmstorefloat2a
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
 - XMStoreFloat2A
 - directxmath/XMStoreFloat2A
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
 - XMStoreFloat2A
---

# XMStoreFloat2A function


## -description

Stores an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> in an <a href="/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)">XMFLOAT2A</a>.

## -parameters

### -param pDestination [out]

Address at which to store the data. The given address must be aligned on a 16-byte boundary.

### -param V [in]

Vector containing the data to store.

## -returns

None.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
return (XMFLOAT2A*)XMStoreVector2A(pDestination, V);
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-storage">DirectXMath Library Vector Store Functions</a>