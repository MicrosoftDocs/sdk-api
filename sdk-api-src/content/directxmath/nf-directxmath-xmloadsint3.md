---
UID: NF:directxmath.XMLoadSInt3
title: XMLoadSInt3 function (directxmath.h)
description: Loads signed integer data into the x, y, and z components of an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadSInt3","XMLoadSInt3","XMLoadSInt3 method [DirectX Math Support APIs]","dxmath.xmloadsint3"]
old-location: dxmath\xmloadsint3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadSInt3(const XMINT3)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadSInt3, XMLoadSInt3, XMLoadSInt3 method [DirectX Math Support APIs], dxmath.xmloadsint3
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
 - XMLoadSInt3
 - directxmath/XMLoadSInt3
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
 - XMLoadSInt3
---

# XMLoadSInt3 function


## -description

Loads signed integer data into the x, y, and z components 
  of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of an <a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a> structure containing the data to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

For 16-byte aligned memory, it may be faster to use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadint3a">XMLoadInt3A</a> 
    with a casting operator.

The following pseudocode shows the operation of this function.


```

XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x;
vectorOut.y = (float)pSource->y;
vectorOut.z = (float)pSource->z;
vectorOut.w = 0;

return vectorOut;
    
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>