---
UID: NF:directxpackedvector.XMLoadUShortN2
title: XMLoadUShortN2 function (directxpackedvector.h)
description: Loads an XMUSHORTN2 into an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadUShortN2","XMLoadUShortN2","XMLoadUShortN2 method [DirectX Math Support APIs]","dxmath.xmloadushortn2"]
old-location: dxmath\xmloadushortn2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUShortN2(const XMUSHORTN2)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadUShortN2, XMLoadUShortN2, XMLoadUShortN2 method [DirectX Math Support APIs], dxmath.xmloadushortn2
req.header: directxpackedvector.h
req.include-header: DirectXMath.h
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
 - XMLoadUShortN2
 - directxpackedvector/XMLoadUShortN2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxpackedvector.h
api_name:
 - XMLoadUShortN2
---

# XMLoadUShortN2 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a> structure to load. This parameter must point to cached
        memory.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x / 65535.0f;
vectorOut.y = (float)pSource->y / 65535.0f;
vectorOut.z = 0;
vectorOut.w = 0;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>