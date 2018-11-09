---
UID: NF:directxmath.XMQuaternionNormalize
title: XMQuaternionNormalize function
author: windows-sdk-content
description: Normalizes a quaternion.
old-location: dxmath\xmquaternionnormalize.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionNormalize(XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMQuaternionNormalize, XMQuaternionNormalize, XMQuaternionNormalize method [DirectX Math Support APIs], dxmath.xmquaternionnormalize
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
 - XMQuaternionNormalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMQuaternionNormalize function


## -description


Normalizes a quaternion.


## -parameters




### -param Q [in]

Quaternion to normalize.


## -returns



Returns the normalized form of <i>Q</i>.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/2d397c98-d0cd-08e0-6104-cca31bb6bd11">DirectXMath Library Quaternion Functions</a>



<a href="https://msdn.microsoft.com/fabc66dc-2930-4ef3-b202-13436176d5a5">XMQuaternionNormalizeEst</a>
 

 

