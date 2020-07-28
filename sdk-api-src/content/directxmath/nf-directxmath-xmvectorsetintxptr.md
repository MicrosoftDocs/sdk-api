---
UID: NF:directxmath.XMVectorSetIntXPtr
title: XMVectorSetIntXPtr function (directxmath.h)
description: Sets the x component of an XMVECTOR containing integer data, with a value contained in an instance of uint32_t referred to by a pointer.
helpviewer_keywords: ["Use DirectX..XMVectorSetIntXPtr","XMVectorSetIntXPtr","XMVectorSetIntXPtr method [DirectX Math Support APIs]","dxmath.xmvectorsetintxptr"]
old-location: dxmath\xmvectorsetintxptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorSetIntXPtr(XMVECTOR,const uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetIntXPtr, XMVectorSetIntXPtr, XMVectorSetIntXPtr method [DirectX Math Support APIs], dxmath.xmvectorsetintxptr
f1_keywords:
- directxmath/XMVectorSetIntXPtr
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
- XMVectorSetIntXPtr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorSetIntXPtr function


## -description


Sets the <code>x</code> component of an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> containing integer data, with a value
  contained in an instance of uint32_t referred to by a pointer.


## -parameters




### -param V

A valid 4D vector storing integer data.


### -param x [in]

Pointer to a uint32_t containing the value to be stored in the <code>x</code> element of the <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>object <code>V</code>.


## -returns



An instance of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> whose <i>x</i> component has been set to the integer value pointed to by
       the argument <i>x</i> of <code>XMVectorSetIntXPtr</code>. All other components of the returned <b>XMVECTOR Data Type</b>instance have the same value as those of the input vector <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>
 

 

