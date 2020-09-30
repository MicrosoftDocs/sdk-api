---
UID: NF:directxpackedvector.XMLoadU555
title: XMLoadU555 function (directxpackedvector.h)
description: Loads an XMU555 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadU555","XMLoadU555","XMLoadU555 method [DirectX Math Support APIs]","dxmath.xmloadu555"]
old-location: dxmath\xmloadu555.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadU555(const XMU555)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadU555, XMLoadU555, XMLoadU555 method [DirectX Math Support APIs], dxmath.xmloadu555
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
 - XMLoadU555
 - directxpackedvector/XMLoadU555
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
 - XMLoadU555
---

# XMLoadU555 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a> structure to load.

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


Note these are not normalized values. To convert to the RGBA 5/5/5/1 format, 
   you must scale the resulting vector by <code>(1.f/31.f, 1.f/31.f, 1.f/31.f, 1.f)</code>. 
   Also, you will probably need to swizzle the standard .x = RED, .y = GREEN, .z =
   BLUE, .w = ALPHA color vector's .x and .z value since the GPU format is BGR (not RGB).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>