---
UID: NF:directxmath.XMVector3NotEqual
title: XMVector3NotEqual function (directxmath.h)
author: windows-sdk-content
description: Tests whether two 3D vectors are not equal.
old-location: dxmath\xmvector3notequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector3NotEqual(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3NotEqual, XMVector3NotEqual, XMVector3NotEqual method [DirectX Math Support APIs], dxmath.xmvector3notequal
ms.topic: function
f1_keywords: 
 - "directxmath/XMVector3NotEqual"
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
 - XMVector3NotEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3NotEqual function


## -description


Tests whether two 3D vectors are not equal.


## -parameters




### -param V1 [in]

3D vector.


### -param V2 [in]

3D vector.


## -returns



Returns true if the 3D vectors are not equal and false otherwise.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
return ( V1.x != V2.x || 
         V1.y != V2.y ||
         V1.z != V2.z;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-comparison">DirectXMath Library 3D Vector Comparison Functions</a>
 

 

