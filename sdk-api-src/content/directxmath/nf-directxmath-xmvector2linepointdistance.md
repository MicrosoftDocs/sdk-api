---
UID: NF:directxmath.XMVector2LinePointDistance
title: XMVector2LinePointDistance function
author: windows-sdk-content
description: Computes the minimum distance between a line and a point.
old-location: dxmath\xmvector2linepointdistance.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2LinePointDistance(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVector2LinePointDistance, XMVector2LinePointDistance, XMVector2LinePointDistance method [DirectX Math Support APIs], dxmath.xmvector2linepointdistance
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
 - XMVector2LinePointDistance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector2LinePointDistance
: 
---

# XMVector2LinePointDistance function


## -description


Computes the minimum distance between a line and a point.


## -parameters




### -param LinePoint1 [in]

2D vector describing a point on the line.


### -param LinePoint2 [in]

2D vector describing a point on the line.


### -param Point [in]

2D vector describing the reference point.


## -returns



Returns a vector. The minimum distance between the line and the point is replicated to each of the components.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/a17cdad7-4fbe-bf83-472f-1b99603b7fec">DirectXMath Library 2D Vector Geometric Functions</a>
 

 

