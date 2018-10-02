---
UID: NF:directxmath.XMVectorMultiplyAdd
title: XMVectorMultiplyAdd function
author: windows-sdk-content
description: Computes the product of the first two vectors added to the third vector.
old-location: dxmath\xmvectormultiplyadd.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorMultiplyAdd(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorMultiplyAdd, XMVectorMultiplyAdd, XMVectorMultiplyAdd method [DirectX Math Support APIs], dxmath.xmvectormultiplyadd
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
 - XMVectorMultiplyAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorMultiplyAdd function


## -description


Computes the product of the first two vectors added to the third vector.


## -parameters




### -param V1 [in]

Vector multiplier.


### -param V2 [in]

Vector multiplicand.


### -param V3 [in]

Vector addend.


## -returns



Returns the product-sum of the vectors.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = V1.x * V2.x + V3.x;
Result.y = V1.y * V2.y+ V3.y;
Result.z = V1.z * V2.z+ V3.z;
Result.w = V1.w * V2.w+ V3.w;

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

