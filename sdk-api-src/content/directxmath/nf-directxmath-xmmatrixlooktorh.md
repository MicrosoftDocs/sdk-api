---
UID: NF:directxmath.XMMatrixLookToRH
title: XMMatrixLookToRH function
author: windows-sdk-content
description: Builds a view matrix for a right-handed coordinate system using a camera position, an up direction, and a camera direction.
old-location: dxmath\xmmatrixlooktorh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixLookToRH(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMMatrixLookToRH, XMMatrixLookToRH, XMMatrixLookToRH method [DirectX Math Support APIs], dxmath.xmmatrixlooktorh
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
 - XMMatrixLookToRH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMatrixLookToRH function


## -description


Builds a view matrix for a right-handed coordinate system using a camera position, an up direction, and a camera direction.


## -parameters




### -param EyePosition [in]

Position of the camera.


### -param EyeDirection [in]

Direction of the camera.


### -param UpDirection [in]

Up direction of the camera, typically &lt; 0.0f, 1.0f, 0.0f &gt;.


## -returns



Returns a view matrix that transforms a point from world space into view space.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>



<a href="https://msdn.microsoft.com/502f1634-e5e4-4247-93f6-449b7f7d6b03">XMMatrixLookToLH</a>
 

 

