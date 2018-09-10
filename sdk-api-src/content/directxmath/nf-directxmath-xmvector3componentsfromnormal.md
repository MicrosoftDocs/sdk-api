---
UID: NF:directxmath.XMVector3ComponentsFromNormal
title: XMVector3ComponentsFromNormal function
author: windows-sdk-content
description: Using a reference normal vector, splits a 3D vector into components that are parallel and perpendicular to the normal.
old-location: dxmath\xmvector3componentsfromnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3ComponentsFromNormal(XMVECTOR@,XMVECTOR@,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVector3ComponentsFromNormal, XMVector3ComponentsFromNormal, XMVector3ComponentsFromNormal method [DirectX Math Support APIs], dxmath.xmvector3componentsfromnormal
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
 - XMVector3ComponentsFromNormal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector3ComponentsFromNormal function


## -description


Using a reference normal vector, splits a 3D vector into components that are parallel and perpendicular to the normal.


## -parameters




### -param pParallel [out]

Address of the component of <i>V</i> that is parallel to <i>Normal</i>.


### -param pPerpendicular [out]

Address of the component of <i>V</i> that is perpendicular to <i>Normal</i>.


### -param V [in]

3D vector to break into components.


### -param Normal [in]

3D reference normal vector.


## -returns



None.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>
 

 

