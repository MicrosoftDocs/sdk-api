---
UID: NF:directxmath.XMMatrixLookAtLH
title: XMMatrixLookAtLH function
author: windows-sdk-content
description: Builds a view matrix for a left-handed coordinate system using a camera position, an up direction, and a focal point.
old-location: dxmath\xmmatrixlookatlh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixLookAtLH(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMMatrixLookAtLH, XMMatrixLookAtLH, XMMatrixLookAtLH method [DirectX Math Support APIs], dxmath.xmmatrixlookatlh
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
 - XMMatrixLookAtLH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMatrixLookAtLH function


## -description


Builds a view matrix for a left-handed coordinate system using a camera position, an up direction, and a focal point.


## -parameters




### -param EyePosition [in]

Position of the camera.


### -param FocusPosition [in]

Position of the focal point.


### -param UpDirection [in]

Up direction of the camera, typically &lt; 0.0f, 1.0f, 0.0f &gt;.


## -returns



Returns a view matrix that transforms a point from world space into view space.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>



<a href="https://msdn.microsoft.com/3367e751-e46f-49a2-a17a-18acec7bd901">XMMatrixLookAtRH</a>
 

 

