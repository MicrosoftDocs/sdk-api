---
UID: NF:directxmath.XMScalarSinCosEst
title: XMScalarSinCosEst function (directxmath.h)
author: windows-sdk-content
description: Estimates both the sine and cosine of a radian angle.
old-location: dxmath\xmscalarsincosest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarSinCosEst(float@,float@,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMScalarSinCosEst, XMScalarSinCosEst, XMScalarSinCosEst method [DirectX Math Support APIs], dxmath.xmscalarsincosest
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
 - XMScalarSinCosEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMScalarSinCosEst function


## -description


Estimates both the sine and cosine of a radian angle.


## -parameters




### -param pSin [out]

Address of a <b>float</b> that will  contain the result of the sine of <i>Value</i>.


### -param pCos [out]

Address of a <b>float</b> that will  contain the result of the cosine of <i>Value</i>.


### -param Value [in]

<b>float</b> value describing the radian angle.


## -returns



This function does not return a value.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses a 7-degree minimax approximation for sine; 6-degree for cosine.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/833273ac-4bbc-029e-df3b-cb860d364cba">DirectXMath Library Scalar Functions</a>



<a href="https://msdn.microsoft.com/f6c08406-ba6a-44e9-816b-51c50ec62bc4">XMScalarSinCos</a>
 

 

