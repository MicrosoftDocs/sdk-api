---
UID: NF:directxcollision.BoundingOrientedBox.CreateFromPoints
title: BoundingOrientedBox::CreateFromPoints
author: windows-sdk-content
description: Creates a BoundingOrientedBox from a collection of points.
old-location: dxmath\boundingorientedbox_createfrompoints.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingOrientedBox.CreateFromPoints(BoundingOrientedBox@,size_t,XMFLOAT3,size_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BoundingOrientedBox interface [DirectX Math Support APIs],CreateFromPoints method, BoundingOrientedBox.CreateFromPoints, BoundingOrientedBox::CreateFromPoints, CreateFromPoints, CreateFromPoints method [DirectX Math Support APIs], CreateFromPoints method [DirectX Math Support APIs],BoundingOrientedBox interface, dxmath.boundingorientedbox_createfrompoints
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
 - BoundingOrientedBox.CreateFromPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingOrientedBox::CreateFromPoints


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Hh855863(v=VS.85).aspx">BoundingOrientedBox</a> from a collection of points.


## -parameters




### -param Out [out, ref]

The new <a href="https://msdn.microsoft.com/en-us/library/Hh855863(v=VS.85).aspx">BoundingOrientedBox</a> containing the specified points.


### -param Count [in]

The number of points in the buffer in <i>pPoints</i>.


### -param pPoints

A buffer containing points to create the <a href="https://msdn.microsoft.com/en-us/library/Hh855863(v=VS.85).aspx">BoundingOrientedBox</a> from.


### -param Stride [in]

The stride of the buffer.


## -returns



This method does not return a value.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh855863(v=VS.85).aspx">BoundingOrientedBox</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh855866(v=VS.85).aspx">Methods</a>



<b>Reference</b>
 

 

