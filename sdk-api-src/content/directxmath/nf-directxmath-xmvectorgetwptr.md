---
UID: NF:directxmath.XMVectorGetWPtr
title: XMVectorGetWPtr function (directxmath.h)
description: Retrieve the w component of an XMVECTOR Data Type containing floating-point data, and storing that component's value in an instance of float referred to by a pointer.
helpviewer_keywords: ["Use DirectX..XMVectorGetWPtr","XMVectorGetWPtr","XMVectorGetWPtr method [DirectX Math Support APIs]","dxmath.xmvectorgetwptr"]
old-location: dxmath\xmvectorgetwptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetWPtr(float@,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorGetWPtr, XMVectorGetWPtr, XMVectorGetWPtr method [DirectX Math Support APIs], dxmath.xmvectorgetwptr
f1_keywords:
- directxmath/XMVectorGetWPtr
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxmathvector.inl
api_name:
- XMVectorGetWPtr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorGetWPtr function


## -description


Retrieve the <code>w</code> component of an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data, and storing that
  component's value in an instance of float referred to by a pointer.


## -parameters




### -param w [out]

Pointer to a float that will receive the value of the <code>w</code> element of the <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> object
        <code>V</code>.


### -param V

A valid 4D vector storing floating-point data.


## -returns



None.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>
 

 

