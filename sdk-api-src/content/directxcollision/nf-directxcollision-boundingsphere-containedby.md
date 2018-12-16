---
UID: NF:directxcollision.BoundingSphere.ContainedBy
title: BoundingSphere::ContainedBy
author: windows-sdk-content
description: Tests whether the BoundingSphere is contained by the specified frustum.
old-location: dxmath\boundingsphere_containedby.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingSphere.ContainedBy(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BoundingSphere interface [DirectX Math Support APIs],ContainedBy method, BoundingSphere.ContainedBy, BoundingSphere::ContainedBy, ContainedBy, ContainedBy method [DirectX Math Support APIs], ContainedBy method [DirectX Math Support APIs],BoundingSphere interface, dxmath.boundingsphere_containedby
ms.topic: method
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
req.namespace: 
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
 - BoundingSphere.ContainedBy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingSphere::ContainedBy


## -description


Tests whether the <a href="https://msdn.microsoft.com/en-us/library/Hh449592(v=VS.85).aspx">BoundingSphere</a> is contained by the specified frustum.


## -parameters




### -param Plane0 [in]

A plane describing the frustum.


### -param Plane1 [in]

A plane describing the frustum.


### -param Plane2 [in]

A plane describing the frustum.


### -param Plane3 [in]

A plane describing the frustum.


### -param Plane4 [in]

A plane describing the frustum.


### -param Plane5 [in]

A plane describing the frustum.


## -returns



A <a href="https://msdn.microsoft.com/en-us/library/Hh449605(v=VS.85).aspx">ContainmentType</a> value indicating whether the frustum contains the <a href="https://msdn.microsoft.com/en-us/library/Hh449592(v=VS.85).aspx">BoundingSphere</a>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh449592(v=VS.85).aspx">BoundingSphere</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a>



<b>Reference</b>
 

 

