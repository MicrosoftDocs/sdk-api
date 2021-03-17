---
UID: NF:directxmath.XMLoadInt3A
title: XMLoadInt3A function (directxmath.h)
description: Loads 16-byte aligned data into the x, y, and z components of an XMVECTOR, without type checking.
helpviewer_keywords: ["Use DirectX..XMLoadInt3A","XMLoadInt3A","XMLoadInt3A method [DirectX Math Support APIs]","dxmath.xmloadint3a"]
old-location: dxmath\xmloadint3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt3A(const VOID)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadInt3A, XMLoadInt3A, XMLoadInt3A method [DirectX Math Support APIs], dxmath.xmloadint3a
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
 - XMLoadInt3A
 - directxmath/XMLoadInt3A
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
 - XMLoadInt3A
---

# XMLoadInt3A function


## -description

Loads 16-byte aligned data into the <b>x</b>, <b>y</b>, and <b>z</b> components of an
  <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>, without type checking.
<div class="alert"><b>Note</b>  This function is provided for backward compatibility with the Xbox Math library. You should use
  <b>XMLoadInt3A</b> when you load integer data, and
  <a href="/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3a">XMLoadFloat3A</a> when you load floating point data.</div><div> </div>

## -parameters

### -param pSource [in]

Address of the 16-byte aligned data to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The w component of the returned <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> is initialized to 0.

To convert the loaded <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> into float values, use
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat">XMConvertVectorUIntToFloat</a> or
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectorinttofloat">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

assert(((uint32_t_PTR)pSource & 0xF) == 0);

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = pElement[2];
V.u[3] = 0;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>
