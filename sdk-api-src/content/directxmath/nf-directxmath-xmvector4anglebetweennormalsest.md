---
UID: NF:directxmath.XMVector4AngleBetweenNormalsEst
title: XMVector4AngleBetweenNormalsEst function
author: windows-sdk-content
description: Estimates the radian angle between two normalized 4D vectors.
old-location: dxmath\xmvector4anglebetweennormalsest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4AngleBetweenNormalsEst(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVector4AngleBetweenNormalsEst, XMVector4AngleBetweenNormalsEst, XMVector4AngleBetweenNormalsEst method [DirectX Math Support APIs], dxmath.xmvector4anglebetweennormalsest
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
 - XMVector4AngleBetweenNormalsEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector4AngleBetweenNormalsEst
: 
---

# XMVector4AngleBetweenNormalsEst function


## -description


Estimates the radian angle between two normalized 4D vectors.


## -parameters




### -param N1 [in]

Normalized 4D vector.


### -param N2 [in]

Normalized 4D vector.


## -returns



Returns a vector. The estimate of the radian angle (between <i>N1</i> and <i>N2</i>) is replicated to each of the components.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/40cf28ab-aa5a-396d-2f9e-2206651966af">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="https://msdn.microsoft.com/4740feb6-a054-4434-b6e8-0f97ad292253">XMVector4AngleBetweenNormals</a>
 

 

