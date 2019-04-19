---
UID: NF:directxmath.XMVector4GreaterR
title: XMVector4GreaterR function (directxmath.h)
author: windows-sdk-content
description: Tests whether one 4D vector is greater than another 4D vector and returns a comparison value that can be examined using functions such as XMComparisonAllTrue.
old-location: dxmath\xmvector4greaterr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector4GreaterR(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4GreaterR, XMVector4GreaterR, XMVector4GreaterR method [DirectX Math Support APIs], dxmath.xmvector4greaterr
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
 - XMVector4GreaterR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector4GreaterR function


## -description


Tests whether one 4D vector is greater than another 4D vector and returns a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/en-us/library/Hh437887(v=VS.85).aspx">XMComparisonAllTrue</a>.


## -parameters




### -param V1 [in]

4D vector.


### -param V2 [in]

4D vector.


## -returns



Returns a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/en-us/library/Hh437887(v=VS.85).aspx">XMComparisonAllTrue</a>.




## -remarks



This function does the following test:


```
V1.x > V2.x
V1.y > V2.y
V1.z > V2.z
V1.w > V2.w
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/1a6d94b8-bb41-cf4a-6e6e-3fc9756f56d2">DirectXMath Library 4D Vector Comparison Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420962(v=VS.85).aspx">XMVector4Greater</a>
 

 

