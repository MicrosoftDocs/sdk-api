---
UID: NF:directxpackedvector.XMLoadByte4
title: XMLoadByte4 function (directxpackedvector.h)
description: Loads an XMBYTE4 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadByte4","XMLoadByte4","XMLoadByte4 method [DirectX Math Support APIs]","dxmath.xmloadbyte4"]
old-location: dxmath\xmloadbyte4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadByte4(const XMBYTE4)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadByte4, XMLoadByte4, XMLoadByte4 method [DirectX Math Support APIs], dxmath.xmloadbyte4
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
 - XMLoadByte4
 - directxpackedvector/XMLoadByte4
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
 - XMLoadByte4
---

# XMLoadByte4 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode demonstrates the operation of the function.


```

XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x;
vectorOut.y = (float)pSource->y;
vectorOut.z = (float)pSource->z;
vectorOut.w = (float)pSource->w;

return vectorOut;

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>