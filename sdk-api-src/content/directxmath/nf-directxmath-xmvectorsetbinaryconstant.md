---
UID: NF:directxmath.XMVectorSetBinaryConstant
title: XMVectorSetBinaryConstant function (directxmath.h)
description: Creates a vector, each of whose components is either 0.0f or 1.0f.
helpviewer_keywords: ["Use DirectX..XMVectorSetBinaryConstant","XMVectorSetBinaryConstant","XMVectorSetBinaryConstant method [DirectX Math Support APIs]","dxmath.xmvectorsetbinaryconstant"]
old-location: dxmath\xmvectorsetbinaryconstant.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.initialization.XMVectorSetBinaryConstant(uint32_t,uint32_t,uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetBinaryConstant, XMVectorSetBinaryConstant, XMVectorSetBinaryConstant method [DirectX Math Support APIs], dxmath.xmvectorsetbinaryconstant
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
 - XMVectorSetBinaryConstant
 - directxmath/XMVectorSetBinaryConstant
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
 - XMVectorSetBinaryConstant
---

# XMVectorSetBinaryConstant function


## -description

Creates a vector, each of whose components is either 0.0f or 1.0f.

## -parameters

### -param C0 [in]

This parameter must be a number (an immediate value, either 0 or 1) and not a variable. If <i>C0</i> is 0, the
        x-component of the returned vector will be 0.0f. Otherwise, the x-component will be 1.0f.

### -param C1 [in]

This parameter must be a number (an immediate value, either 0 or 1) and not a variable. If <i>C1</i> is 0, the
        y-component of the returned vector will be 0.0f. Otherwise, the y-component will be 1.0f.

### -param C2 [in]

This parameter must be a number (an immediate value, either 0 or 1) and not a variable. If <i>C2</i> is 0, the
        z-component of the returned vector will be 0.0f. Otherwise, the z-component will be 1.0f.

### -param C3 [in]

This parameter must be a number (an immediate value, either 0 or 1) and not a variable. If <i>C3</i> is 0, the
        w-component of the returned vector will be 0.0f. Otherwise, the w-component will be 1.0f.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>, each of whose components is either 0.0f or 1.0f.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-initialization">Vector Initialization Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsetint">XMVectorSetInt</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsplatconstant">XMVectorSplatConstant</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsplatconstantint">XMVectorSplatConstantInt</a>