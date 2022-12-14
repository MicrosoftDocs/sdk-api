---
UID: NF:directxmath.XMLoadInt4
title: XMLoadInt4 function (directxmath.h)
description: Loads data into an XMVECTOR, without type checking.
helpviewer_keywords: ["Use DirectX..XMLoadInt4","XMLoadInt4","XMLoadInt4 method [DirectX Math Support APIs]","dxmath.xmloadint4"]
old-location: dxmath\xmloadint4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt4(const VOID)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadInt4, XMLoadInt4, XMLoadInt4 method [DirectX Math Support APIs], dxmath.xmloadint4
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
 - XMLoadInt4
 - directxmath/XMLoadInt4
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
 - XMLoadInt4
---

# XMLoadInt4 function


## -description

Loads data into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>, without type checking.
<div class="alert"><b>Note</b>  This function is provided for backward compatibility with the Xbox Math library. 
  You should use 
 <b>XMLoadInt4</b> when you load integer data, and
  <a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadfloat4">XMLoadFloat4</a> when you load floating point data.</div><div> </div>

## -parameters

### -param pSource [in]

Address of the data to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

To convert the loaded <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> into float values, use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat">XMConvertVectorUIntToFloat</a> or <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectorinttofloat">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = pElement[2];
V.u[3] = pElement[3];

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>



<a href="/windows/desktop/direct3dhlsl/xmint4">XMINT4</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmloadsint4">XMLoadSInt4</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmloaduint4">XMLoadUInt4</a>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint4">XMUINT4</a>