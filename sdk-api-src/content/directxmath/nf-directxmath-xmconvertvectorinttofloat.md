---
UID: NF:directxmath.XMConvertVectorIntToFloat
title: XMConvertVectorIntToFloat function (directxmath.h)
description: Converts an XMVECTOR with int32_t components to an XMVECTOR with float components and applies a uniform bias.
helpviewer_keywords: ["Use DirectX..XMConvertVectorIntToFloat","XMConvertVectorIntToFloat","XMConvertVectorIntToFloat method [DirectX Math Support APIs]","dxmath.xmconvertvectorinttofloat"]
old-location: dxmath\xmconvertvectorinttofloat.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.conversion.XMConvertVectorIntToFloat(XMVECTOR,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMConvertVectorIntToFloat, XMConvertVectorIntToFloat, XMConvertVectorIntToFloat method [DirectX Math Support APIs], dxmath.xmconvertvectorinttofloat
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
 - XMConvertVectorIntToFloat
 - directxmath/XMConvertVectorIntToFloat
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
 - XMConvertVectorIntToFloat
---

# XMConvertVectorIntToFloat function


## -description

Converts an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> with <b>int32_t</b> components to an
  <b>XMVECTOR</b> with <b>float</b> components and applies a uniform bias.

## -parameters

### -param VInt [in]

Vector with <b>int32_t</b> components that is to be converted.

### -param DivExponent [in]

Each component of <i>VInt</i> will be converted to a <b>float</b> and then divided by two raised to the
        <i>DivExponent</i> power. This parameter must be a number (an immediate value) and not a variable.

## -returns

Returns the converted vector, where each component has been divided by two raised to the <i>DivExponent</i> power.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-conversion">DirectXMath Library Conversion Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectorfloattoint">XMConvertVectorFloatToInt</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat">XMConvertVectorUIntToFloat</a>