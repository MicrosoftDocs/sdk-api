---
UID: NF:directxmath.XMVectorSinCos
title: XMVectorSinCos function
author: windows-sdk-content
description: Computes the sine and cosine of each component of an XMVECTOR.
old-location: dxmath\xmvectorsincos.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorSinCos(XMVECTOR@,XMVECTOR@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorSinCos, XMVectorSinCos, XMVectorSinCos method [DirectX Math Support APIs], dxmath.xmvectorsincos
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
 - XMVectorSinCos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorSinCos function


## -description


Computes the sine and cosine of each component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSin [out]

Address of a vector, each of whose components is the sine of the corresponding component of <i>V</i>.


### -param pCos [out]

Address of a vector, each of whose components is the cosine of the corresponding component of <i>V</i>.


### -param V [in]

Vector for which to compute the sine and cosine.


## -returns



None.




## -remarks



This function uses an 11-degree minimax approximation for sine, 10-degree for cosine.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/b450ecd2-1668-4006-b0ef-e1aa57e5a972">XMVectorSinCosEst</a>
 

 

