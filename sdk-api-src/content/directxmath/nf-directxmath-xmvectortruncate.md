---
UID: NF:directxmath.XMVectorTruncate
title: XMVectorTruncate function
author: windows-sdk-content
description: Rounds each component of a vector to the nearest integer value in the direction of zero.
old-location: dxmath\xmvectortruncate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorTruncate(XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorTruncate, XMVectorTruncate, XMVectorTruncate method [DirectX Math Support APIs], dxmath.xmvectortruncate
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
 - XMVectorTruncate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorTruncate
: 
---

# XMVectorTruncate function


## -description


Rounds each component of a vector to the nearest integer value in the direction of zero.


## -parameters




### -param V [in]

Vector whose components are to be truncated.


## -returns



Returns a vector whose components are rounded to the nearest integer value in the direction of zero.




## -remarks



The return value is computed based on the following logic, which preserves special values (INF,+INF,NaN,-NaN).

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Result[0] = (fabsf(V[0]) &lt; 8388608.0f) ? ((float)((int32_t)V[0])) : V[0];
Result[1] = (fabsf(V[1]) &lt; 8388608.0f) ? ((float)((int32_t)V[1])) : V[1];
Result[2] = (fabsf(V[2]) &lt; 8388608.0f) ? ((float)((int32_t)V[2])) : V[2];
Result[3] = (fabsf(V[3]) &lt; 8388608.0f) ? ((float)((int32_t)V[3])) : V[3];
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

