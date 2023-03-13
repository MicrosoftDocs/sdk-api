---
UID: NF:directxmath.XMVectorSetIntW
title: XMVectorSetIntW function (directxmath.h)
description: Set the value of the w component of an XMVECTOR Data Type. (XMVectorSetIntW)
helpviewer_keywords: ["Use DirectX..XMVectorSetIntW","XMVectorSetIntW","XMVectorSetIntW method [DirectX Math Support APIs]","dxmath.xmvectorsetintw"]
old-location: dxmath\xmvectorsetintw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorSetIntW(XMVECTOR,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetIntW, XMVectorSetIntW, XMVectorSetIntW method [DirectX Math Support APIs], dxmath.xmvectorsetintw
req.header: directxmath.h
req.include-header: DirectXMath.h
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
 - XMVectorSetIntW
 - directxmath/XMVectorSetIntW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorSetIntW
---

# XMVectorSetIntW function


## -description

Set the value of the <code>w</code> component of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>.

## -parameters

### -param V [in]

A valid 4D unsigned integer vector.

### -param w [in]

A unsigned integer value to be assigned to <code>w</code> of <i>V</i>.

## -returns

An instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> whose <i>x</i> component has been set to the integer value provided by
       the argument <i>x</i> to <code>XMVectorSetIntW</code>. All other components of the returned <b>XMVECTOR Data Type</b> instance have the same value as those of the input vector <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>
