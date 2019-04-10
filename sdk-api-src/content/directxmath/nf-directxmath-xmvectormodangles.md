---
UID: NF:directxmath.XMVectorModAngles
title: XMVectorModAngles function (directxmath.h)
author: windows-sdk-content
description: Computes the per-component angle modulo 2PI.
old-location: dxmath\xmvectormodangles.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorModAngles(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorModAngles, XMVectorModAngles, XMVectorModAngles method [DirectX Math Support APIs], dxmath.xmvectormodangles
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
 - XMVectorModAngles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorModAngles function


## -description


Computes the per-component angle modulo 2PI.


## -parameters




### -param Angles [in]

Vector of angle components.


## -returns



Returns a vector whose components are the corresponding components of <i>Angles</i> modulo 2PI.




## -remarks



The following pseudocode demonstrates the operation of the function:


```
XMVECTOR result;

result.x = Angles.x - XM_2PI * round( Angles.x / XM_2PI );
result.y = Angles.y - XM_2PI * round( Angles.y / XM_2PI );
result.z = Angles.z - XM_2PI * round( Angles.z / XM_2PI );
result.w = Angles.w - XM_2PI * round( Angles.w / XM_2PI );

return result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

