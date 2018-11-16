---
UID: NF:directxmath.XMMatrixOrthographicOffCenterRH
title: XMMatrixOrthographicOffCenterRH function
author: windows-sdk-content
description: Builds a custom orthogonal projection matrix for a right-handed coordinate system.
old-location: dxmath\xmmatrixorthographicoffcenterrh.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixOrthographicOffCenterRH(float,float,float,float,float,float)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMMatrixOrthographicOffCenterRH, XMMatrixOrthographicOffCenterRH, XMMatrixOrthographicOffCenterRH method [DirectX Math Support APIs], dxmath.xmmatrixorthographicoffcenterrh
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
 - XMMatrixOrthographicOffCenterRH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMMatrixOrthographicOffCenterRH
: 
---

# XMMatrixOrthographicOffCenterRH function


## -description


Builds a custom orthogonal projection matrix for a right-handed coordinate system.


## -parameters




### -param ViewLeft [in]

Minimum x-value of the view volume.


### -param ViewRight [in]

Maximum x-value of the view volume.


### -param ViewBottom [in]

Minimum y-value of the view volume.


### -param ViewTop [in]

Maximum y-value of the view volume.


### -param NearZ [in]

Distance to the near clipping plane. 


### -param FarZ [in]

Distance to the far clipping plane. 


## -returns



Returns the custom orthogonal projection matrix.




## -remarks



All the parameters of <b>XMMatrixOrthographicOffCenterRH</b> are
   distances in camera space.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>



<a href="https://msdn.microsoft.com/ae9de21b-c5c7-48da-8f97-1fa3ec19b83b">XMMatrixOrthographicOffCenterLH</a>
 

 

