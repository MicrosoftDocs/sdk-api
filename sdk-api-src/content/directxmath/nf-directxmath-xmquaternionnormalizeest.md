---
UID: NF:directxmath.XMQuaternionNormalizeEst
title: XMQuaternionNormalizeEst function (directxmath.h)
author: windows-sdk-content
description: Estimates the normalized version of a quaternion.
old-location: dxmath\xmquaternionnormalizeest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionNormalizeEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionNormalizeEst, XMQuaternionNormalizeEst, XMQuaternionNormalizeEst method [DirectX Math Support APIs], dxmath.xmquaternionnormalizeest
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
 - XMQuaternionNormalizeEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMQuaternionNormalizeEst function


## -description


Estimates the normalized version of a quaternion.


## -parameters




### -param Q [in]

A quaternion for which to estimate the normalized version.


## -returns



An <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> union that is the estimate of the normalized version of a quaternion.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

This function internally calls the <a href="https://msdn.microsoft.com/en-us/library/Ee420977(v=VS.85).aspx">XMVector4NormalizeEst</a>function.

<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/2d397c98-d0cd-08e0-6104-cca31bb6bd11">DirectXMath Library Quaternion Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420168(v=VS.85).aspx">XMQuaternionNormalize</a>
 

 

