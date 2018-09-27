---
UID: NF:directxmath.XMMatrixOrthographicLH
title: XMMatrixOrthographicLH function
author: windows-sdk-content
description: Builds an orthogonal projection matrix for a left-handed coordinate system.
old-location: dxmath\xmmatrixorthographiclh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixOrthographicLH(float,float,float,float)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMMatrixOrthographicLH, XMMatrixOrthographicLH, XMMatrixOrthographicLH method [DirectX Math Support APIs], dxmath.xmmatrixorthographiclh
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
 - XMMatrixOrthographicLH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMatrixOrthographicLH function


## -description


Builds an orthogonal projection matrix for a left-handed coordinate system.


## -parameters




### -param ViewWidth [in]

Width of the frustum at the near clipping plane.


### -param ViewHeight [in]

Height of the frustum at the near clipping plane.


### -param NearZ [in]

Distance to the near clipping plane. 


### -param FarZ [in]

Distance to the far clipping plane. 


## -returns



Returns the orthogonal projection matrix.




## -remarks



All the parameters of
   <b>XMMatrixOrthographicLH</b> are distances
   in camera space.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>



<a href="https://msdn.microsoft.com/1a339f6e-dddb-4bd7-b5db-e26ea8e41118">XMMatrixOrthographicRH</a>
 

 

