---
UID: NF:directxcollision.BoundingFrustum.ContainedBy
title: ContainedBy function
author: windows-sdk-content
description: Tests whether a triangle is contained within six planes (typically a frustum).
old-location: dxmath\containedby.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.TriangleTests.ContainedBy(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ContainedBy, ContainedBy method [DirectX Math Support APIs], DirectX::TriangleTests.ContainedBy, dxmath.containedby
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxcollision.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: DirectX::TriangleTests
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
 - DirectXCollision.h
api_name:
 - ContainedBy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ContainedBy function


## -description


Tests whether a triangle is contained within six planes (typically a frustum).


## -parameters




### -param Plane0

A vector defining a plane.


### -param Plane1

A vector defining a plane.


### -param Plane2

A vector defining a plane.


### -param Plane3

A vector defining a plane.


### -param Plane4

A vector defining a plane.


### -param Plane5

A vector defining a plane.


#### - V0

A vector defining the triangle.


#### - V1

A vector defining the triangle.


#### - V2

A vector defining the triangle.


## -returns



A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> value indicating whether the triangle is contained within the planes.




## -remarks



<div class="alert"><b>Note</b>  <code>TriangleTests</code>::<code>ContainedBy</code> is new for DirectXMath.  This functionality is not available in XNAMath 2.x.  
  Similar functionality for XNAMath can be found in the DirectX SDK Collision sample.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/97c5fa38-e88c-debb-f3ed-76c5878778c4">DirectXMath Triangle Test Functions</a>
 

 

