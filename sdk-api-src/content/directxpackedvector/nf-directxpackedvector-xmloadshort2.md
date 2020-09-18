---
UID: NF:directxpackedvector.XMLoadShort2
title: XMLoadShort2 function (directxpackedvector.h)
description: Loads an XMSHORT2 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadShort2","XMLoadShort2","XMLoadShort2 method [DirectX Math Support APIs]","dxmath.xmloadshort2"]
old-location: dxmath\xmloadshort2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadShort2(const XMSHORT2)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadShort2, XMLoadShort2, XMLoadShort2 method [DirectX Math Support APIs], dxmath.xmloadshort2
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
 - XMLoadShort2
 - directxpackedvector/XMLoadShort2
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
 - XMLoadShort2
---

# XMLoadShort2 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> structure loaded with the data from the <i>pSource</i> parameter.

## -remarks

The <b>x</b> and <b>y</b> members of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> are converted to
   single-precision format, and loaded into the corresponding members of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. The
   <b>z</b> and <b>w</b> members of the returned <b>XMVECTOR</b> will be initialized to 0. The
   following pseudocode shows you the operation of this function:


```
XMVECTOR Result;

Result.x = (float)pSource->x;
Result.y = (float)pSource->y;
vectorOut.z = 0;
vectorOut.w = 0;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>