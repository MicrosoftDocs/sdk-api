---
UID: NF:directxmath.XMVector3ReciprocalLengthEst
title: XMVector3ReciprocalLengthEst function
author: windows-sdk-content
description: Estimates the reciprocal of the length of a 3D vector.
old-location: dxmath\xmvector3reciprocallengthest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3ReciprocalLengthEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVector3ReciprocalLengthEst, XMVector3ReciprocalLengthEst, XMVector3ReciprocalLengthEst method [DirectX Math Support APIs], dxmath.xmvector3reciprocallengthest
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
 - XMVector3ReciprocalLengthEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector3ReciprocalLengthEst function


## -description


Estimates the reciprocal of the length of a 3D vector.


## -parameters




### -param V [in]

3D vector.


## -returns



Returns a vector, each of whose components are estimates of the reciprocal of the length of <i>V</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>



<a href="https://msdn.microsoft.com/a8797240-57b3-4ee8-8a15-32d651f3f498">XMVector3ReciprocalLength</a>
 

 

