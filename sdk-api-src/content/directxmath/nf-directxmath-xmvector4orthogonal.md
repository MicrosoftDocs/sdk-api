---
UID: NF:directxmath.XMVector4Orthogonal
title: XMVector4Orthogonal function
author: windows-sdk-content
description: Computes a vector perpendicular to a 4D vector.
old-location: dxmath\xmvector4orthogonal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4Orthogonal(XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector4Orthogonal, XMVector4Orthogonal, XMVector4Orthogonal method [DirectX Math Support APIs], dxmath.xmvector4orthogonal
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
 - XMVector4Orthogonal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector4Orthogonal
: 
---

# XMVector4Orthogonal function


## -description


Computes a vector perpendicular to a 4D vector.


## -parameters




### -param V [in]

4D vector.


## -returns



Returns the 4D vector orthogonal to <i>V</i>.




## -remarks



A 4D cross-product is not well-defined. This function computes a generalized 'cross-product' for 4D vectors. 
    <a href="https://msdn.microsoft.com/61cc3f3b-171a-4a67-b588-ea242b1a6110">XMVector4Cross</a> is another geometric 'cross-product' for 4D vectors.

The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
XMVECTOR Result;

Result.x = V.z;
Result.y = V.w;
Result.z = -V.x;
Result.w = -V.y;

return Result;
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/40cf28ab-aa5a-396d-2f9e-2206651966af">DirectXMath Library 4D Vector Geometric Functions</a>
 

 

