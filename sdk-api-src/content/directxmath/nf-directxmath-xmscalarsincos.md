---
UID: NF:directxmath.XMScalarSinCos
title: XMScalarSinCos function
author: windows-sdk-content
description: Computes both the sine and cosine of a radian angle.
old-location: dxmath\xmscalarsincos.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarSinCos(float@,float@,float)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMScalarSinCos, XMScalarSinCos, XMScalarSinCos method [DirectX Math Support APIs], dxmath.xmscalarsincos
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
 - XMScalarSinCos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMScalarSinCos function


## -description


Computes both the sine and cosine of a radian angle.


## -parameters




### -param pSin [out]

Address of a <b>float</b> that will contain the result of the sine of <i>Value</i>.


### -param pCos [out]

Address of a <b>float</b> that will contain the result of the cosine of <i>Value</i>.


### -param Value [in]

<b>float</b> value describing the radian angle.


## -returns



This function does not return a value.




## -remarks



This function uses a 11-degree minimax approximation for sine; 10-degree for cosine.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/833273ac-4bbc-029e-df3b-cb860d364cba">DirectXMath Library Scalar Functions</a>



<a href="https://msdn.microsoft.com/ff564017-6ce4-48b4-ac54-31b858b37e5f">XMScalarSinCosEst</a>
 

 

