---
UID: NF:directxpackedvector.XMLoadUDecN4
title: XMLoadUDecN4 function (directxpackedvector.h)
description: Loads an XMUDECN4 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadUDecN4","XMLoadUDecN4","XMLoadUDecN4 method [DirectX Math Support APIs]","dxmath.xmloadudecn4"]
old-location: dxmath\xmloadudecn4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUDecN4(const XMUDECN4)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadUDecN4, XMLoadUDecN4, XMLoadUDecN4 method [DirectX Math Support APIs], dxmath.xmloadudecn4
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
 - XMLoadUDecN4
 - directxpackedvector/XMLoadUDecN4
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
 - XMLoadUDecN4
---

# XMLoadUDecN4 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

uint32_t Element;

Element = pSource->v & 0x3FF;
vectorOut.x = (float)Element / 1023.f;
Element = (pSource->v >> 10) & 0x3FF;
vectorOut.y = (float)Element / 1023.f;
Element = (pSource->v >> 20) & 0x3FF;
vectorOut.z = (float)Element / 1023.f;
vectorOut.w = (float)(pSource->v >> 30) / 3.f;

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>