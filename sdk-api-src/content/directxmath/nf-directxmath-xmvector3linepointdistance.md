---
UID: NF:directxmath.XMVector3LinePointDistance
title: XMVector3LinePointDistance function
author: windows-sdk-content
description: Computes the minimum distance between a line and a point.
old-location: dxmath\xmvector3linepointdistance.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3LinePointDistance(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector3LinePointDistance, XMVector3LinePointDistance, XMVector3LinePointDistance method [DirectX Math Support APIs], dxmath.xmvector3linepointdistance
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
 - XMVector3LinePointDistance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector3LinePointDistance
: 
---

# XMVector3LinePointDistance function


## -description


Computes the minimum distance between a line and a point.


## -parameters




### -param LinePoint1 [in]

3D vector describing a point on the line.


### -param LinePoint2 [in]

3D vector describing a point on the line.


### -param Point [in]

3D vector describing the reference point.


## -returns



Returns a vector. The minimum distance between the line and the point is replicated to each of the components.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>
 

 

