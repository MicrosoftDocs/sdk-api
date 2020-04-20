---
UID: NF:directxmath.XMLoadInt
title: XMLoadInt function (directxmath.h)
description: Loads a scalar value into an XMVECTOR.helpviewer_keywords: ["Use DirectX..XMLoadInt","XMLoadInt","XMLoadInt method [DirectX Math Support APIs]","dxmath.xmloadint"]
old-location: dxmath\xmloadint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt(const uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadInt, XMLoadInt, XMLoadInt method [DirectX Math Support APIs], dxmath.xmloadint
f1_keywords:
- directxmath/XMLoadInt
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXMath.h
api_name:
- XMLoadInt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMLoadInt function


## -description


Loads a scalar value into an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the scalar data to load.


## -returns



Returns an <code>XMVECTORI</code> whose <b>x</b> member is loaded with the data from
       the <i>pSource</i> parameter. The other components of the returned vector will be initialized to 0.




## -remarks



To convert the loaded <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> into float values, use <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat">XMConvertVectorUIntToFloat</a> or <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectorinttofloat">XMConvertVectorIntToFloat</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>
 

 

