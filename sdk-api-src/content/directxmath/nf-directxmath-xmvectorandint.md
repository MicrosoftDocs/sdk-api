---
UID: NF:directxmath.XMVectorAndInt
title: XMVectorAndInt function
author: windows-sdk-content
description: Computes the logical AND of two vectors, treating each component as an unsigned integer.
old-location: dxmath\xmvectorandint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.bit-wise.XMVectorAndInt(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorAndInt, XMVectorAndInt, XMVectorAndInt method [DirectX Math Support APIs], dxmath.xmvectorandint
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
 - XMVectorAndInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorAndInt function


## -description


Computes the logical AND of two vectors, treating each component as an unsigned integer.


## -parameters




### -param V1 [in]

First vector.


### -param V2 [in]

Second vector.


## -returns



Returns a vector each of whose components are the logical AND of the corresponding components of <i>V1</i> and <i>V2</i>.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = V1.x &amp; V2.x;
Result.y = V1.y &amp; V2.y;
Result.z = V1.z &amp; V2.z;
Result.w = V1.w &amp; V2.w;

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/c28ade14-3cf8-3d8e-260b-58751caea8d0">Bit-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/e7c78708-1261-4907-9fbe-3226b587ed57">XMVectorAndCInt</a>
 

 

