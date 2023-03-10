---
UID: NF:directxpackedvector.XMLoadColor
title: XMLoadColor function (directxpackedvector.h)
description: Loads an XMCOLOR into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadColor","XMLoadColor","XMLoadColor method [DirectX Math Support APIs]","dxmath.xmloadcolor"]
old-location: dxmath\xmloadcolor.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadColor(const XMCOLOR)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadColor, XMLoadColor, XMLoadColor method [DirectX Math Support APIs], dxmath.xmloadcolor
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
 - XMLoadColor
 - directxpackedvector/XMLoadColor
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
 - XMLoadColor
---

# XMLoadColor function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter with X containing 
	   the Red color channel, Y containing the Green, Z the Blue, and W the Alpha channel. The values in the components range from 0 to 1.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)((pSource->c >> 16) & 0xFF) / 255.0f;
vectorOut.y = (float)((pSource->c >> 8) & 0xFF) / 255.0f;
vectorOut.z = (float)((pSource->c >> 0) & 0xFF) / 255.0f;
vectorOut.w = (float)((pSource->c >> 24) & 0xFF) / 255.0f;

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>