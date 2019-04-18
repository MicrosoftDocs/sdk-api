---
UID: NF:directxmath.XMVectorSqrtEst
title: XMVectorSqrtEst function (directxmath.h)
author: windows-sdk-content
description: Estimates the per-component square root of a vector.
old-location: dxmath\xmvectorsqrtest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorSqrtEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSqrtEst, XMVectorSqrtEst, XMVectorSqrtEst method [DirectX Math Support APIs], dxmath.xmvectorsqrtest
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
 - XMVectorSqrtEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorSqrtEst function


## -description


Estimates the per-component square root of a vector.


## -parameters




### -param V [in]

Vector whose square root is estimated.


## -returns



Returns a vector. Each component is an estimate of the square-root of the corresponding component of <i>V</i>.




## -remarks



The square-root operation handles special input values as follows.

<table>
<tr>
<th>Input Value</th>
<th>Return Value</th>
</tr>
<tr>
<td>+Infinity</td>
<td>+Infinity</td>
</tr>
<tr>
<td>+0.0f</td>
<td>+0.0f</td>
</tr>
<tr>
<td>-0.0f</td>
<td>-0.0f</td>
</tr>
<tr>
<td>&lt; 0.0f</td>
<td>QNaN*</td>
</tr>
</table>
 

* Note that due to implementation details, VMX128 returns -Infinity in this case instead of the standard QNaN.

<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee421356(v=VS.85).aspx">XMVectorSqrt</a>
 

 

