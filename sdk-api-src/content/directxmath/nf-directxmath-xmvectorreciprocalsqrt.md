---
UID: NF:directxmath.XMVectorReciprocalSqrt
title: XMVectorReciprocalSqrt function
author: windows-sdk-content
description: Computes the per-component reciprocal square root of a vector.
old-location: dxmath\xmvectorreciprocalsqrt.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorReciprocalSqrt(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorReciprocalSqrt, XMVectorReciprocalSqrt, XMVectorReciprocalSqrt method [DirectX Math Support APIs], dxmath.xmvectorreciprocalsqrt
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
 - XMVectorReciprocalSqrt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorReciprocalSqrt function


## -description


Computes the per-component reciprocal square root of a vector.


## -parameters




### -param V [in]

Vector whose reciprocal square root is computed.


## -returns



Returns a vector. Each component is the reciprocal square-root of the corresponding component of <i>V</i>.




## -remarks



The reciprocal square-root operation handles special input values as follows.

<table>
<tr>
<th>Input Value</th>
<th>Return Value</th>
</tr>
<tr>
<td>+Infinity</td>
<td>0*</td>
</tr>
<tr>
<td>+0.0f</td>
<td>+Infinity*</td>
</tr>
<tr>
<td>-0.0f</td>
<td>-Infinity*</td>
</tr>
<tr>
<td>&lt; 0.0f</td>
<td>QNaN</td>
</tr>
</table>
 

* Note that due to implementation details, VMX128 returns QNaN in all special cases.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>



<a href="https://msdn.microsoft.com/6204b326-a02f-4477-8aef-18a8870fbdb7">XMVectorReciprocalSqrtEst</a>
 

 

