---
UID: NF:directxmath.XMVectorGetXPtr
title: XMVectorGetXPtr function (directxmath.h)
description: Retrieve the x component of an XMVECTOR Data Type containing floating-point data, and storing that component's value in an instance of float referred to by a pointer.
helpviewer_keywords: ["Use DirectX..XMVectorGetXPtr","XMVectorGetXPtr","XMVectorGetXPtr method [DirectX Math Support APIs]","dxmath.xmvectorgetxptr"]
old-location: dxmath\xmvectorgetxptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetXPtr(float@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorGetXPtr, XMVectorGetXPtr, XMVectorGetXPtr method [DirectX Math Support APIs], dxmath.xmvectorgetxptr
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
 - XMVectorGetXPtr
 - directxmath/XMVectorGetXPtr
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
 - XMVectorGetXPtr
---

# XMVectorGetXPtr function


## -description

Retrieve the <code>x</code> component of an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data, and storing that
  component's value in an instance of float referred to by a pointer.

## -parameters

### -param x [out]

Pointer to a float that will receive the value of the <code>x</code> element of the <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> object
        <code>V</code>.

### -param V

A valid 4D vector storing floating-point data.

## -returns

None.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>