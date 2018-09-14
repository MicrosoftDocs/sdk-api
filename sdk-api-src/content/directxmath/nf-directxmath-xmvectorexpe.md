---
UID: NF:directxmath.XMVectorExpE
title: XMVectorExpE function
author: windows-sdk-content
description: Computes e (~2.71828) raised to the power for each component.
old-location: dxmath\xmvectorexpe.htm
tech.root: dxmath
ms.assetid: C4A5E4E0-56CC-46E3-87C5-CA99EF512B11
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorExpE, XMVectorExpE, XMVectorExpE method [DirectX Math Support APIs], dxmath.xmvectorexpe
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
 - XMVectorExpE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorExpE function


## -description


Computes e (~2.71828) raised to the power for each component.


## -parameters




### -param V [in]

Vector used for the exponents of base e.


## -returns



Returns a vector whose components are e raised to the power of the corresponding component of <i>V</i>.





## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.1. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorExpE</b> is new for DirectXMath version 3.05. 

It's similar to the existing <a href="https://msdn.microsoft.com/c9d97292-49ee-4c55-92b4-bcc851cfd23b">XMVectorExp</a> function for Windows 8, but computes base e instead of base 2.


<b>XMVectorExpE</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result; 

Result.x = expf(V.x);
Result.y = expf(V.y);
Result.z = expf(V.z);
Result.w = expf(V.w);

return Result;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/1B04528B-532B-4555-B027-D5EC33DD9843">XMVectorExp2</a>



<a href="https://msdn.microsoft.com/C092B786-BAB8-4F8F-95D2-3C23F59EF064">XMVectorLogE</a>
 

 

