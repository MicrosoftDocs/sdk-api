---
UID: NF:directxmath.XMVectorClamp
title: XMVectorClamp function
author: windows-sdk-content
description: Clamps the components of a vector to a specified minimum and maximum range.
old-location: dxmath\xmvectorclamp.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.arithmetic.XMVectorClamp(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVectorClamp, XMVectorClamp, XMVectorClamp method [DirectX Math Support APIs], dxmath.xmvectorclamp
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
 - XMVectorClamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorClamp function


## -description


Clamps the components of a vector to a specified minimum and maximum range.


## -parameters




### -param V [in]

Vector whose components are to be clamped.


### -param Min [in]

Minimum range vector.


### -param Max [in]

Maximum range vector.


## -returns



Returns a vector whose components are clamped to the specified minimum and maximum values.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = min( max( V.x, Min.x ), Max.x );
Result.y = min( max( V.y, Min.y ), Max.y );
Result.z = min( max( V.z, Min.z ), Max.z );
Result.w = min( max( V.w, Min.w ), Max.w );

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d7ed4516-74a6-81ec-79a2-2e39cf112d11">Vector Arithmetic Functions</a>
 

 

