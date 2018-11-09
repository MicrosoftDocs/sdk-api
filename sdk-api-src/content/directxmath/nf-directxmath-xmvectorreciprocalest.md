---
UID: NF:directxmath.XMVectorReciprocalEst
title: XMVectorReciprocalEst function
author: windows-sdk-content
description: Estimates the per-component reciprocal of a vector.
old-location: dxmath\xmvectorreciprocalest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorReciprocalEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVectorReciprocalEst, XMVectorReciprocalEst, XMVectorReciprocalEst method [DirectX Math Support APIs], dxmath.xmvectorreciprocalest
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
 - XMVectorReciprocalEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorReciprocalEst function


## -description


Estimates the per-component reciprocal of a vector.


## -parameters




### -param V [in]

Vector whose reciprocal is estimated.


## -returns



Returns a vector. Each component is an estimate of the reciprocal of the corresponding component of <i>V</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>



<a href="https://msdn.microsoft.com/0d2ab2a8-60b0-43ca-9993-31aadaaa66e9">XMVectorReciprocal</a>
 

 

