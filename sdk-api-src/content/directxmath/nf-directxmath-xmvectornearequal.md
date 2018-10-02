---
UID: NF:directxmath.XMVectorNearEqual
title: XMVectorNearEqual function
author: windows-sdk-content
description: Performs a per-component test for equality of two vectors within a given threshold.
old-location: dxmath\xmvectornearequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorNearEqual(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorNearEqual, XMVectorNearEqual, XMVectorNearEqual method [DirectX Math Support APIs], dxmath.xmvectornearequal
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
 - XMVectorNearEqual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorNearEqual function


## -description


Performs a per-component test for equality of two vectors within a given threshold. 


## -parameters




### -param V1 [in]

First vector to compare.


### -param V2 [in]

Second vector compare.


### -param Epsilon [in]

Tolerance value used for judging equality.


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

Result.x = (abs(V1.x - V2.x) &lt;= Epsilon) ? 0xFFFFFFFF : 0;
Result.y = (abs(V1.y - V2.y) &lt;= Epsilon) ? 0xFFFFFFFF : 0;
Result.z = (abs(V1.z - V2.z) &lt;= Epsilon) ? 0xFFFFFFFF : 0;
Result.w = (abs(V1.w - V2.w) &lt;= Epsilon) ? 0xFFFFFFFF : 0;

return Result;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/8caad40f-ab8e-db2f-da11-18f3d3ccf6ef">Vector Comparison Functions</a>
 

 

