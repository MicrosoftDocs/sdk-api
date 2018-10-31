---
UID: NF:directxmath.XMVectorLog2
title: XMVectorLog2 function
author: windows-sdk-content
description: Computes the base two logarithm of each component of a vector.
old-location: dxmath\xmvectorlog2.htm
tech.root: dxmath
ms.assetid: 92C911B4-5BC7-443D-BCBB-F4838E24E607
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorLog2, XMVectorLog2, XMVectorLog2 method [DirectX Math Support APIs], dxmath.xmvectorlog2
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
 - XMVectorLog2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorLog2
: 
---

# XMVectorLog2 function


## -description


Computes the base two logarithm of each component of a vector.


## -parameters




### -param V [in]

Vector for which to compute the base two logarithm.


## -returns



Returns a vector whose components are base two logarithm of the corresponding components of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorLog2</b> is new for DirectXMath version 3.05, but it's just a renamed version of the existing <a href="https://msdn.microsoft.com/fbc211d2-1cde-4145-9439-2bcccd763358">XMVectorLog</a> function for Windows 8. 



<b>XMVectorLog2</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result;

Result.x = logf(V.x) / logf(2);
Result.y = logf(V.y) / logf(2);
Result.z = logf(V.z) / logf(2);
Result.w = logf(V.w) / logf(2);

return Result;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/1B04528B-532B-4555-B027-D5EC33DD9843">XMVectorExp2</a>



<a href="https://msdn.microsoft.com/C092B786-BAB8-4F8F-95D2-3C23F59EF064">XMVectorLogE</a>
 

 

