---
UID: NF:directxmath.XMPlaneDot
title: XMPlaneDot function
author: windows-sdk-content
description: Calculates the dot product between an input plane and a 4D vector.
old-location: dxmath\xmplanedot.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneDot(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMPlaneDot, XMPlaneDot, XMPlaneDot method [DirectX Math Support APIs], dxmath.xmplanedot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
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
 - DirectXMath.h
api_name:
 - XMPlaneDot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMPlaneDot
: 
---

# XMPlaneDot function


## -description


Calculates the dot product between an input plane and a 4D vector.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.


### -param V [in]

4D vector to use in the dot product.


## -returns



Returns the dot product of <i>P</i> and <i>V</i> replicated into each of the four components of the returned
       <b>XMVECTOR</b>.




## -remarks



The <b>XMPlaneDot</b> function is useful for determining the
   plane's relationship with a homogeneous coordinate. For example, this function can be used to determine if a
   particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>
 

 

