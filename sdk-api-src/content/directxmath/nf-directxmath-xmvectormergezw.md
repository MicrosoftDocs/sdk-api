---
UID: NF:directxmath.XMVectorMergeZW
title: XMVectorMergeZW function
author: windows-sdk-content
description: Creates a new vector by combining the z and w-components of two vectors.
old-location: dxmath\xmvectormergezw.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorMergeZW(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorMergeZW, XMVectorMergeZW, XMVectorMergeZW method [DirectX Math Support APIs], dxmath.xmvectormergezw
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
 - XMVectorMergeZW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorMergeZW function


## -description


Creates a new vector by combining the z and w-components of two vectors.


## -parameters




### -param V1 [in]

First vector.


### -param V2 [in]

Second vector.


## -returns



Returns the merged vector.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = V1.z;
Result.y = V2.z;
Result.z = V1.w;
Result.w = V2.w;

return Result;
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f5464614-f6bb-427d-5488-3ba0fd4c6e8d">Component-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/925fb6b1-5588-437f-b753-2fa51257f67e">XMVectorMergeXY</a>
 

 

