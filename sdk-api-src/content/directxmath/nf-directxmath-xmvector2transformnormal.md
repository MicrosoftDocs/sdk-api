---
UID: NF:directxmath.XMVector2TransformNormal
title: XMVector2TransformNormal function
author: windows-sdk-content
description: Transforms the 2D vector normal by the given matrix.
old-location: dxmath\xmvector2transformnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2TransformNormal(XMVECTOR,XMMATRIX)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector2TransformNormal, XMVector2TransformNormal, XMVector2TransformNormal method [DirectX Math Support APIs], dxmath.xmvector2transformnormal
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
 - XMVector2TransformNormal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector2TransformNormal function


## -description


Transforms the 2D vector normal by the given matrix.


## -parameters




### -param V [in]

2D normal vector.


### -param M [in]

Transformation matrix.


## -returns



Returns the transformed vector.




## -remarks



<code>XMVector2TransformNormal</code> uses row 0 and 1 of the input transformation matrix for rotation and scaling. Rows 2 and 3 are ignored.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/175c2073-40ac-06b5-2f0e-495bd74b1502">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/9f8e9987-e31d-4baa-a463-18e61f25ee2f">XMVector2TransformNormalStream</a>
 

 

