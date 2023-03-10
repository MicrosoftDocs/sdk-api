---
UID: NF:directxmath.XMLoadInt2
title: XMLoadInt2 function (directxmath.h)
description: Loads data into the x and y components of an XMVECTOR.
helpviewer_keywords: ["Use DirectX..XMLoadInt2","XMLoadInt2","XMLoadInt2 method [DirectX Math Support APIs]","dxmath.xmloadint2"]
old-location: dxmath\xmloadint2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt2(const uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadInt2, XMLoadInt2, XMLoadInt2 method [DirectX Math Support APIs], dxmath.xmloadint2
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
 - XMLoadInt2
 - directxmath/XMLoadInt2
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
 - XMLoadInt2
---

# XMLoadInt2 function


## -description

Loads data into the x and y components of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the data to load.

## -returns

Returns an <code>XMVECTORI</code> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The z and w components of the returned <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> will be initialized to 0.

For 16-byte aligned memory, it may be faster to use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadint2a">XMLoadInt2A</a> with a casting operator.

To convert the loaded <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> into float values, use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat">XMConvertVectorUIntToFloat</a> or <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectorinttofloat">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = 0;
V.u[3] = 0;

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmint2">XMINT2</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadsint2">XMLoadSInt2</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmloaduint2">XMLoadUInt2</a>



<a href="/windows/desktop/direct3dhlsl/xmuint2">XMUINT2</a>