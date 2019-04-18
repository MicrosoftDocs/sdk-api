---
UID: NF:directxmath.XMPlaneNormalizeEst
title: XMPlaneNormalizeEst function (directxmath.h)
author: windows-sdk-content
description: Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.
old-location: dxmath\xmplanenormalizeest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneNormalizeEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneNormalizeEst, XMPlaneNormalizeEst, XMPlaneNormalizeEst method [DirectX Math Support APIs], dxmath.xmplanenormalizeest
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
 - XMPlaneNormalizeEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMPlaneNormalizeEst function


## -description


Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.


## -returns



Returns an estimation of the normalized plane as a 4D vector whose components are the plane coefficients (A, B, C, D) 
        for the plane equation <code>Ax+By+Cz+D=0</code>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420148(v=VS.85).aspx">XMPlaneNormalize</a>
 

 

