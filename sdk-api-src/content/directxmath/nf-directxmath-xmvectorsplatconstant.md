---
UID: NF:directxmath.XMVectorSplatConstant
title: XMVectorSplatConstant function (directxmath.h)
description: Creates a vector with identical floating-point components. Each component is a constant divided by two raised to an integer exponent.
helpviewer_keywords: ["Use DirectX..XMVectorSplatConstant","XMVectorSplatConstant","XMVectorSplatConstant method [DirectX Math Support APIs]","dxmath.xmvectorsplatconstant"]
old-location: dxmath\xmvectorsplatconstant.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.initialization.XMVectorSplatConstant(uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSplatConstant, XMVectorSplatConstant, XMVectorSplatConstant method [DirectX Math Support APIs], dxmath.xmvectorsplatconstant
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
 - XMVectorSplatConstant
 - directxmath/XMVectorSplatConstant
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
 - XMVectorSplatConstant
---

# XMVectorSplatConstant function


## -description

Creates a vector with identical floating-point components. Each component is a constant divided by two raised to an
  integer exponent.

## -parameters

### -param IntConstant [in]

This value will be converted to a floating-point number and divided by two raised to the <i>DivExponent</i> power.
        The result is replicated to each component of the returned vector.

The value of <i>IntConstant</i> must satisfy: -16 &lt;= <i>IntConstant</i> &lt;=15.

<div class="alert"><b>Note</b>  This parameter must be a number (an immediate value) and not a variable.</div>
<div> </div>

### -param DivExponent [in]

Describes the exponent applied to the quotient. This parameter must be a number (an immediate value) and not a
        variable.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> with identical floating-point components. Each component is a constant
       divided by two raised to an integer exponent.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-initialization">Vector Initialization Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsetbinaryconstant">XMVectorSetBinaryConstant</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsetint">XMVectorSetInt</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsplatconstantint">XMVectorSplatConstantInt</a>