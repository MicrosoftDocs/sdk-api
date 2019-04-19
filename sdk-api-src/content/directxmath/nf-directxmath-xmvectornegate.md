---
UID: NF:directxmath.XMVectorNegate
title: XMVectorNegate function (directxmath.h)
author: windows-sdk-content
description: Computes the negation of a vector.
old-location: dxmath\xmvectornegate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorNegate(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorNegate, XMVectorNegate, XMVectorNegate method [DirectX Math Support APIs], dxmath.xmvectornegate
ms.topic: function
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
 - XMVectorNegate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorNegate function


## -description


Computes the negation of a vector.


## -parameters




### -param V [in]

Vector to negate.


## -returns



Returns the negation of the vector.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR result;

result.x = -V.x;
result.y = -V.y;
result.z = -V.z;
result.w = -V.w;

return result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

