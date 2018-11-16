---
UID: NF:directxmath.XMVectorIsNaN
title: XMVectorIsNaN function
author: windows-sdk-content
description: Performs a per-component NaN test on a vector.
old-location: dxmath\xmvectorisnan.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorIsNaN(XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVectorIsNaN, XMVectorIsNaN, XMVectorIsNaN method [DirectX Math Support APIs], dxmath.xmvectorisnan
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMVectorIsNaN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorIsNaN
: 
---

# XMVectorIsNaN function


## -description


Performs a per-component NaN test on a vector.


## -parameters




### -param V [in]

Vector to test.


## -returns



Returns a vector containing the results of each component test.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = (V.x == SNaN || V.x == QNaN) ? 0xFFFFFFFF : 0;
Result.y = (V.y == SNaN || V.y == QNaN) ? 0xFFFFFFFF : 0;
Result.z = (V.z == SNaN || V.z == QNaN) ? 0xFFFFFFFF : 0;
Result.w = (V.w == SNaN || V.w == QNaN) ? 0xFFFFFFFF : 0;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

