---
UID: NF:directxmath.XMVectorFloor
title: XMVectorFloor function (directxmath.h)
author: windows-sdk-content
description: Computes the floor of each component of an XMVECTOR.
old-location: dxmath\xmvectorfloor.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorFloor(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorFloor, XMVectorFloor, XMVectorFloor method [DirectX Math Support APIs], dxmath.xmvectorfloor
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
 - XMVectorFloor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVectorFloor function


## -description


Computes the floor of each component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the floor.


## -returns



Returns a vector whose components are the floor of the corresponding components of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

<b>XMVectorFloor</b> is implemented like this:

<pre class="syntax" xml:space="preserve"><code>
XMVECTOR Result;
Result.x = floorf(V.x);
Result.y = floorf(V.y);
Result.z = floorf(V.z);
Result.w = floorf(V.w);
return Result;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee421007(v=VS.85).aspx">XMVectorCeiling</a>
 

 

