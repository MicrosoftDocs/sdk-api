---
UID: NF:directxmath.XMQuaternionSquad
title: XMQuaternionSquad function
author: windows-sdk-content
description: Interpolates between four unit quaternions, using spherical quadrangle interpolation.
old-location: dxmath\xmquaternionsquad.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionSquad(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,float)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMQuaternionSquad, XMQuaternionSquad, XMQuaternionSquad method [DirectX Math Support APIs], dxmath.xmquaternionsquad
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
 - XMQuaternionSquad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMQuaternionSquad function


## -description


Interpolates between four unit quaternions, using spherical quadrangle interpolation.


## -parameters




### -param Q0 [in]

First unit quaternion.


### -param Q1 [in]

Second unit quaternion.


### -param Q2 [in]

Third unit quaternion.


### -param Q3 [in]

Fourth unit quaternion.


### -param t [in]

Interpolation control factor.


## -returns



Returns the interpolated quaternion. If <i>Q0</i>, <i>Q1</i>, <i>Q2</i>, and <i>Q3</i> are not all unit
       quaternions, the returned quaternion is undefined.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

The use of this method requires some setup before its use. See
   <a href="https://msdn.microsoft.com/c50ee260-e111-43d5-9484-d7fec4d938be">XMQuaternionSquadSetup</a> for details.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/2d397c98-d0cd-08e0-6104-cca31bb6bd11">DirectXMath Library Quaternion Functions</a>



<a href="https://msdn.microsoft.com/c50ee260-e111-43d5-9484-d7fec4d938be">XMQuaternionSquadSetup</a>



<a href="https://msdn.microsoft.com/6B6D298A-9647-41CF-9E15-BDFBDE964999">XMQuaternionSquadV</a>
 

 

