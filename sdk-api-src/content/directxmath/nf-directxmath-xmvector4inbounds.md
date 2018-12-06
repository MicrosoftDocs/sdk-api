---
UID: NF:directxmath.XMVector4InBounds
title: XMVector4InBounds function
author: windows-sdk-content
description: Tests whether the components of a 4D vector are within set bounds.
old-location: dxmath\xmvector4inbounds.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4InBounds(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVector4InBounds, XMVector4InBounds, XMVector4InBounds method [DirectX Math Support APIs], dxmath.xmvector4inbounds
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
 - XMVector4InBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector4InBounds function


## -description


Tests whether the components of a 4D vector are within set bounds.


## -parameters




### -param V [in]

4D vector to test.


### -param Bounds [in]

4D vector that determines the bounds.


## -returns



Returns true if all of the components of <i>V</i> are within the set bounds, and false otherwise.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>return (V.x &lt;= Bounds.x &amp;&amp; V.x &gt;= -Bounds.x) &amp;&amp;
       (V.y &lt;= Bounds.y &amp;&amp; V.y &gt;= -Bounds.y) &amp;&amp;
       (V.z &lt;= Bounds.z &amp;&amp; V.z &gt;= -Bounds.z) &amp;&amp;
       (V.w &lt;= Bounds.w &amp;&amp; V.w &gt;= -Bounds.w);</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/40cf28ab-aa5a-396d-2f9e-2206651966af">DirectXMath Library 4D Vector Geometric Functions</a>
 

 

