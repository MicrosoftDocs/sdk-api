---
UID: NF:directxmath.XMVectorExp2
title: XMVectorExp2 function
author: windows-sdk-content
description: Computes two raised to the power for each component.
old-location: dxmath\xmvectorexp2.htm
tech.root: dxmath
ms.assetid: 1B04528B-532B-4555-B027-D5EC33DD9843
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVectorExp2, XMVectorExp2, XMVectorExp2 method [DirectX Math Support APIs], dxmath.xmvectorexp2
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
 - XMVectorExp2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorExp2 function


## -description


Computes two raised to the power for each component.


## -parameters




### -param V [in]

Vector used for the exponents of base two.


## -returns



Returns a vector whose components are two raised to the power of the corresponding component of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorExp2</b> is new for DirectXMath version 3.05, but it's just a renamed version of the existing <a href="https://msdn.microsoft.com/c9d97292-49ee-4c55-92b4-bcc851cfd23b">XMVectorExp</a> function for Windows 8. 



<b>XMVectorExp2</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result; 

Result.x = powf(2.0f, V.x);
Result.y = powf(2.0f, V.y);
Result.z = powf(2.0f, V.z);
Result.w = powf(2.0f, V.w);

return Result;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/C4A5E4E0-56CC-46E3-87C5-CA99EF512B11">XMVectorExpE</a>



<a href="https://msdn.microsoft.com/92C911B4-5BC7-443D-BCBB-F4838E24E607">XMVectorLog2</a>
 

 

