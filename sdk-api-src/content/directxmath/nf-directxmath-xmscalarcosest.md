---
UID: NF:directxmath.XMScalarCosEst
title: XMScalarCosEst function (directxmath.h)
author: windows-sdk-content
description: Estimates the cosine of a radian angle.
old-location: dxmath\xmscalarcosest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.scalar.XMScalarCosEst(float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMScalarCosEst, XMScalarCosEst, XMScalarCosEst method [DirectX Math Support APIs], dxmath.xmscalarcosest
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
 - XMScalarCosEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMScalarCosEst function


## -description


Estimates the cosine of a radian angle.


## -parameters




### -param Value [in]

<b>float</b> value describing the radian angle.


## -returns



Returns the cosine of <i>Value</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses a 6-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/833273ac-4bbc-029e-df3b-cb860d364cba">DirectXMath Library Scalar Functions</a>



<a href="https://msdn.microsoft.com/bea42d18-69f2-4045-83e1-25106b2094a0">XMScalarACos</a>



<a href="https://msdn.microsoft.com/4b5578fb-590a-4ced-957a-0e214941530a">XMScalarACosEst</a>



<a href="https://msdn.microsoft.com/7ad12f5a-0ab1-4d59-bdb3-ffe045abc2aa">XMScalarCos</a>
 

 

