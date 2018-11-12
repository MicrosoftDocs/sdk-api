---
UID: NF:directxmath.XMVector2EqualR
title: XMVector2EqualR function
author: windows-sdk-content
description: Tests whether two 2D vectors are equal. In addition, this function returns a comparison value that can be examined using functions such as XMComparisonAllTrue.
old-location: dxmath\xmvector2equalr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVector2EqualR(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVector2EqualR, XMVector2EqualR, XMVector2EqualR method [DirectX Math Support APIs], dxmath.xmvector2equalr
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
 - XMVector2EqualR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector2EqualR function


## -description


Tests whether two 2D vectors are equal. In addition, this function returns a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>.


## -parameters




### -param V1 [in]

2D vector.


### -param V2 [in]

2D vector.


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
<pre>V1.x == V2.x
V1.y == V2.y</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/16e8348b-c6cf-06a5-12be-5954de3522c1">DirectXMath Library 2D Vector Comparison Functions</a>



<a href="https://msdn.microsoft.com/7d4439e3-b1ae-4ee8-babe-f75c12f10010">XMVector2Equal</a>
 

 

