---
UID: NF:directxmath.XMVectorSetIntZPtr
title: XMVectorSetIntZPtr function (directxmath.h)
description: Sets the z component of an XMVECTOR containing integer data, with a value contained in an instance of uint32_t referred to by a pointer.
helpviewer_keywords: ["Use DirectX..XMVectorSetIntZPtr","XMVectorSetIntZPtr","XMVectorSetIntZPtr method [DirectX Math Support APIs]","dxmath.xmvectorsetintzptr"]
old-location: dxmath\xmvectorsetintzptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorSetIntZPtr(XMVECTOR,const uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetIntZPtr, XMVectorSetIntZPtr, XMVectorSetIntZPtr method [DirectX Math Support APIs], dxmath.xmvectorsetintzptr
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
 - XMVectorSetIntZPtr
 - directxmath/XMVectorSetIntZPtr
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
 - XMVectorSetIntZPtr
---

# XMVectorSetIntZPtr function


## -description

Sets the <code>z</code> component of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> containing integer data, with a value
  contained in an instance of uint32_t referred to by a pointer.

## -parameters

### -param V

A valid 4D vector storing integer data.

### -param z [in]

Pointer to a uint32_t containing the value to be stored in the <code>z</code> element of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> object <code>V</code>.

## -returns

An instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> whose <i>z</i> component has been set to the integer value pointed to by
       the argument <i>z</i> of <code>XMVectorSetIntZPtr</code>. All other components of the returned <b>XMVECTOR Data Type</b> instance have the same value as those of the input vector <i>V</i>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>