---
UID: NF:directxmath.XMVector3GreaterOrEqualR
title: XMVector3GreaterOrEqualR function
author: windows-sdk-content
description: Tests whether one 3D vector is greater-than-or-equal-to another 3D vector and returns a comparison value that can be examined using functions such as XMComparisonAllTrue.
old-location: dxmath\xmvector3greaterorequalr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector3GreaterOrEqualR(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVector3GreaterOrEqualR, XMVector3GreaterOrEqualR, XMVector3GreaterOrEqualR method [DirectX Math Support APIs], dxmath.xmvector3greaterorequalr
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
 - XMVector3GreaterOrEqualR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector3GreaterOrEqualR function


## -description


Tests whether one 3D vector is greater-than-or-equal-to another 3D vector and returns a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>.


## -parameters




### -param V1 [in]

3D vector.


### -param V2 [in]

3D vector.


## -returns



Returns a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>.




## -remarks



This function does the following test:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>V1.x &gt;= V2.x
V1.y &gt;= V2.y
V1.z &gt;= V2.z</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/8c5f71fd-2ef8-86db-42de-da3da3c17e41">DirectXMath Library 3D Vector Comparison Functions</a>



<a href="https://msdn.microsoft.com/67057b1e-b954-4cd4-9167-7a18b1aae477">XMVector3GreaterOrEqual</a>
 

 

