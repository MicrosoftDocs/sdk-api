---
UID: NF:directxpackedvector.XMLoadShort4
title: XMLoadShort4 function (directxpackedvector.h)
description: Loads an XMSHORT4 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadShort4","XMLoadShort4","XMLoadShort4 method [DirectX Math Support APIs]","dxmath.xmloadshort4"]
old-location: dxmath\xmloadshort4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadShort4(const XMSHORT4)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadShort4, XMLoadShort4, XMLoadShort4 method [DirectX Math Support APIs], dxmath.xmloadshort4
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
 - XMLoadShort4
 - directxpackedvector/XMLoadShort4
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
 - XMLoadShort4
---

# XMLoadShort4 function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> structure loaded with the data from the <i>pSource</i> parameter.

## -remarks

The four members of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> 
   are converted to single-precision format, and loaded into the corresponding members 
   of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. The following pseudocode demonstrates
   the operation of this function:


```
XMVECTOR Result;

Result.x = (float)pSource->x;
Result.y = (float)pSource->y;
Result.z = (float)pSource->z;
Result.w = (float)pSource->w;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>