---
UID: NF:directxmath.XMVectorLogE
title: XMVectorLogE function
author: windows-sdk-content
description: Computes the base e logarithm of each component of a vector.
old-location: dxmath\xmvectorloge.htm
tech.root: dxmath
ms.assetid: C092B786-BAB8-4F8F-95D2-3C23F59EF064
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorLogE, XMVectorLogE, XMVectorLogE method [DirectX Math Support APIs], dxmath.xmvectorloge
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
 - XMVectorLogE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorLogE function


## -description


Computes the base e logarithm of each component of a vector.The base e logarithm is also known as the natural logarithm.


## -parameters




### -param V [in]

Vector for which to compute the base e logarithm.


## -returns



Returns a vector whose components are base e logarithm of the corresponding components of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorLogE</b> is new for DirectXMath version 3.05. 

It's similar to the existing <a href="https://msdn.microsoft.com/en-us/library/Ee421175(v=VS.85).aspx">XMVectorLog</a> function for Windows 8, but computes base e instead of base 2.


<b>XMVectorLogE</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result;

Result.x = logf(V.x);
Result.y = logf(V.y);
Result.z = logf(V.z);
Result.w = logf(V.w);

return Result;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/C4A5E4E0-56CC-46E3-87C5-CA99EF512B11">XMVectorExpE</a>



<a href="https://msdn.microsoft.com/92C911B4-5BC7-443D-BCBB-F4838E24E607">XMVectorLog2</a>
 

 

