---
UID: NF:directxmath.XMVectorACos
title: XMVectorACos function
author: windows-sdk-content
description: Computes the arccosine of each component of an XMVECTOR.
old-location: dxmath\xmvectoracos.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorACos(XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVectorACos, XMVectorACos, XMVectorACos method [DirectX Math Support APIs], dxmath.xmvectoracos
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
 - XMVectorACos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorACos
: 
---

# XMVectorACos function


## -description


Computes the arccosine of each component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the arccosine. Each component should be between -1.0f and 1.0f.


## -returns



Returns a vector whose components are the arccosine of the corresponding components of <i>V</i>.




## -remarks



This function uses a 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/162da582-d82f-4c48-995f-3c3750ea8df1">XMVectorACosEst</a>



<a href="https://msdn.microsoft.com/87ccfa3f-4770-4fde-b575-80e39d509426">XMVectorCos</a>



<a href="https://msdn.microsoft.com/8c7ee39d-76b5-476a-bfa0-ab77594e114c">XMVectorCosEst</a>
 

 

