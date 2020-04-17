---
UID: NF:directxmath.XMVectorDivide
title: XMVectorDivide function (directxmath.h)
description: Divides one instance of XMVECTOR by a second instance, returning the result in a third instance.helpviewer_keywords: ["Use DirectX..XMVectorDivide","XMVectorDivide","XMVectorDivide method [DirectX Math Support APIs]","dxmath.xmvectordivide"]
old-location: dxmath\xmvectordivide.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorDivide(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorDivide, XMVectorDivide, XMVectorDivide method [DirectX Math Support APIs], dxmath.xmvectordivide
f1_keywords:
- directxmath/XMVectorDivide
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
- XMVectorDivide
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorDivide function


## -description


Divides one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.

The <code>XMVectorDivide</code> divides each component of an instance of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> by the corresponding component in a
  second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.


## -parameters




### -param V1 [in]

<code>XMVECTOR</code> instance whose components are the <i>dividends</i> of the division operation.


### -param V2 [in]

<code>XMVECTOR</code> instance whose components are the <i>divisors</i> of the division operation.


## -returns



<code>XMVECTOR</code> instance whose components are the <i>quotient</i> of the division of each component of
       <b>V1</b> by each corresponding component of <b>V2</b>.




## -remarks



The following code is generally faster than calling <code>XMVectorDivide</code> if the loss of precision is tolerable.


```

XMVECTOR R = XMVectorReciprocalEst(V2)    
XMVectorMultiply(V1,R)
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>
 

 

