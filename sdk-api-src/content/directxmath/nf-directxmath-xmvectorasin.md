---
UID: NF:directxmath.XMVectorASin
title: XMVectorASin function
author: windows-sdk-content
description: Computes the arcsine of each component of an XMVECTOR.
old-location: dxmath\xmvectorasin.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorASin(XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVectorASin, XMVectorASin, XMVectorASin method [DirectX Math Support APIs], dxmath.xmvectorasin
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
 - XMVectorASin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorASin function


## -description


Computes the arcsine of each component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the arcsine. Each component should be between -1.0f and 1.0f.


## -returns



Returns a vector whose components are the arcsine of the corresponding components of <i>V</i>.




## -remarks



This function uses a 7-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/1cffeed1-7214-491d-8434-38f9d6269f0e">XMVectorASinEst</a>



<a href="https://msdn.microsoft.com/5f1c424a-1fef-42dd-9976-49f79372076d">XMVectorSin</a>
 

 

