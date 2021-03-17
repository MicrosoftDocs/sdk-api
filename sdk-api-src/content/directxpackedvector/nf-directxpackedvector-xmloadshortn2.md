---
UID: NF:directxpackedvector.XMLoadShortN2
title: XMLoadShortN2 function (directxpackedvector.h)
description: Loads an XMSHORTN2 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadShortN2","XMLoadShortN2","XMLoadShortN2 method [DirectX Math Support APIs]","dxmath.xmloadshortn2"]
old-location: dxmath\xmloadshortn2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadShortN2(const XMSHORTN2)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadShortN2, XMLoadShortN2, XMLoadShortN2 method [DirectX Math Support APIs], dxmath.xmloadshortn2
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
 - XMLoadShortN2
 - directxpackedvector/XMLoadShortN2
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
 - XMLoadShortN2
---

# XMLoadShortN2 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> structure to load. This parameter must point to cached
        memory.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x / 32767.0f;
vectorOut.y = (float)pSource->y / 32767.0f;
vectorOut.z = 0;
vectorOut.w = 0;

return vectorOut;
```


Note that both -32767 and -32768 map to -1.f.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>