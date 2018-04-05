---
UID: NF:directxcollision.BoundingFrustum.Intersects
title: Intersects function
author: windows-driver-content
description: Tests whether a triangle and a plane intersect.
old-location: dxmath\intersects_1.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.TriangleTests.Intersects(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: DirectX::TriangleTests.Intersects, Intersects, Intersects method [DirectX Math Support APIs], dxmath.intersects_1
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectXCollision.h
api_name:
-	Intersects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Intersects function


## -description


Tests whether a triangle and a plane intersect.


## -parameters




### -param sh

TBD




#### - Plane

A vector defining a plane.


#### - V0

A vector defining a triangle.


#### - V1

A vector defining a triangle.


#### - V2

A vector defining a triangle.


## -returns



A <a href="https://msdn.microsoft.com/66191FCC-F0A0-4435-86A9-0662A5E36D83">PlaneIntersectionType</a> value indicating whether the triangle intersects the plane.




## -remarks



<div class="alert"><b>Note</b>  <code>TriangleTests</code>::<code>Intersects</code> is new for DirectXMath.  This functionality is not available in XNAMath 2.x.  
  Similar functionality for XNAMath can be found in the DirectX SDK Collision sample.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/97c5fa38-e88c-debb-f3ed-76c5878778c4">DirectXMath Triangle Test Functions</a>
 

 

