---
UID: NF:directxmath.XMVectorLerpV
title: XMVectorLerpV function
author: windows-sdk-content
description: Performs a linear interpolation between two vectors.
old-location: dxmath\xmvectorlerpv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorLerpV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVectorLerpV, XMVectorLerpV, XMVectorLerpV method [DirectX Math Support APIs], dxmath.xmvectorlerpv
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
 - XMVectorLerpV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorLerpV
: 
---

# XMVectorLerpV function


## -description


Performs a linear interpolation between two vectors.


## -parameters




### -param V0 [in]

First vector to interpolate from.


### -param V1 [in]

Second vector to interpolate from.


### -param T [in]

Interpolating control factor for the corresponding components of the position.


## -returns



Returns a vector containing the interpolation.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = V0.x + T.x * (V1.x - V0.x);
Result.y = V0.y + T.y * (V1.y - V0.y);
Result.z = V0.z + T.z * (V1.z - V0.z);
Result.w = V0.w + T.w * (V1.w - V0.w);

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/7c941454-7410-f3fb-d750-9007f672ed8c">Geometric Vector Functions</a>



<a href="https://msdn.microsoft.com/2f82e49a-d551-4b64-8325-31c84805165c">XMVectorLerp</a>
 

 

