---
UID: NF:directxmath.XMVectorLessOrEqual
title: XMVectorLessOrEqual function
author: windows-sdk-content
description: Performs a per-component test for less-than-or-equal between two vectors.
old-location: dxmath\xmvectorlessorequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorLessOrEqual(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorLessOrEqual, XMVectorLessOrEqual, XMVectorLessOrEqual method [DirectX Math Support APIs], dxmath.xmvectorlessorequal
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
 - XMVectorLessOrEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorLessOrEqual function


## -description


Performs a per-component test for less-than-or-equal between two vectors.


## -parameters




### -param V1 [in]

First vector to compare.


### -param V2 [in]

Second vector to compare.


## -returns



Returns a vector containing the results of each component test.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = (V1.x &lt;= V2.x) ? 0xFFFFFFFF : 0;
Result.y = (V1.y &lt;= V2.y) ? 0xFFFFFFFF : 0;
Result.z = (V1.z &lt;= V2.z) ? 0xFFFFFFFF : 0;
Result.w = (V1.w &lt;= V2.w) ? 0xFFFFFFFF : 0;

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/8caad40f-ab8e-db2f-da11-18f3d3ccf6ef">Vector Comparison Functions</a>
 

 

