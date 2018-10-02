---
UID: NF:directxmath.XMVectorRound
title: XMVectorRound function
author: windows-sdk-content
description: Rounds each component of a vector to the nearest even integer (known as &#0034;Bankers Rounding&#0034;).
old-location: dxmath\xmvectorround.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorRound(XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorRound, XMVectorRound, XMVectorRound method [DirectX Math Support APIs], dxmath.xmvectorround
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
 - XMVectorRound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorRound function


## -description


Rounds each component of a vector to the nearest even integer (known as "Bankers Rounding").


## -parameters




### -param V [in]

Vector whose components should be rounded.


## -returns



Returns a vector, each of whose components are rounded to the nearest integer.




## -remarks



Banker's Rounding is used because it is the native vector rounding intrinsic method for both SSE4 and ARMv8 NEON.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

