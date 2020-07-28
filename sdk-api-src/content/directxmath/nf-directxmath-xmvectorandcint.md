---
UID: NF:directxmath.XMVectorAndCInt
title: XMVectorAndCInt function (directxmath.h)
description: Computes the logical AND of one vector with the negation of a second vector, treating each component as an unsigned integer.
helpviewer_keywords: ["Use DirectX..XMVectorAndCInt","XMVectorAndCInt","XMVectorAndCInt method [DirectX Math Support APIs]","dxmath.xmvectorandcint"]
old-location: dxmath\xmvectorandcint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.bit-wise.XMVectorAndCInt(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorAndCInt, XMVectorAndCInt, XMVectorAndCInt method [DirectX Math Support APIs], dxmath.xmvectorandcint
f1_keywords:
- directxmath/XMVectorAndCInt
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
- XMVectorAndCInt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorAndCInt function


## -description


Computes the logical AND of one vector with the negation of a second vector, treating each component as an unsigned integer.


## -parameters




### -param V1 [in]

First vector.


### -param V2 [in]

Second vector.


## -returns



Returns a vector whose components are the logical AND of each of the components of <i>V1</i> with the negation of the corresponding components of <i>V2</i>.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = V1.x & ~V2.x;
Result.y = V1.y & ~V2.y;
Result.z = V1.z & ~V2.z;
Result.w = V1.w & ~V2.w;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-bit-wise">Bit-Wise Vector Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvectorandint">XMVectorAndInt</a>
 

 

