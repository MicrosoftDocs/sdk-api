---
UID: NF:directxmath.XMVector3Equal
title: XMVector3Equal function (directxmath.h)
description: Tests whether two 3D vectors are equal.helpviewer_keywords: ["Use DirectX..XMVector3Equal","XMVector3Equal","XMVector3Equal method [DirectX Math Support APIs]","dxmath.xmvector3equal"]
old-location: dxmath\xmvector3equal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector3Equal(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Equal, XMVector3Equal, XMVector3Equal method [DirectX Math Support APIs], dxmath.xmvector3equal
f1_keywords:
- directxmath/XMVector3Equal
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
- XMVector3Equal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3Equal function


## -description


Tests whether two 3D vectors are equal.


## -parameters




### -param V1 [in]

3D vector.


### -param V2 [in]

3D vector.


## -returns



Returns true if the 3D vectors are equal and false otherwise.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
return ( V1.x == V2.x && 
         V1.y == V2.y &&
         V1.z == V2.z );
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-comparison">DirectXMath Library 3D Vector Comparison Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvector3equalr">XMVector3EqualR</a>
 

 

