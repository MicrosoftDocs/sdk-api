---
UID: NF:directxmath.XMFresnelTerm
title: XMFresnelTerm function
author: windows-sdk-content
description: Calculates the Fresnel term for unpolarized light.
old-location: dxmath\xmfresnelterm.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.utilities.XMFresnelTerm(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMFresnelTerm, XMFresnelTerm, XMFresnelTerm method [DirectX Math Support APIs], dxmath.xmfresnelterm
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
 - XMFresnelTerm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMFresnelTerm function


## -description


Calculates the Fresnel term for unpolarized light.


## -parameters




### -param CosIncidentAngle [in]

Vector consisting of the cosines of the incident angles.


### -param RefractionIndex [in]

Vector consisting of the refraction indices of the materials corresponding to the incident angles.


## -returns



Returns a vector containing the Fresnel term of each component.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/4d46fd96-55ca-cb66-f878-caf7894535ae">DirectXMath Library Utility Functions</a>
 

 

