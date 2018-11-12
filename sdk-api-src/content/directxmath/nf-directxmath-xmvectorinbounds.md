---
UID: NF:directxmath.XMVectorInBounds
title: XMVectorInBounds function
author: windows-sdk-content
description: Tests whether the components of a given vector are within set bounds.
old-location: dxmath\xmvectorinbounds.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorInBounds(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVectorInBounds, XMVectorInBounds, XMVectorInBounds method [DirectX Math Support APIs], dxmath.xmvectorinbounds
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
 - XMVectorInBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorInBounds function


## -description


Tests whether the components of a given vector are within set bounds.


## -parameters




### -param V [in]

Vector to test.


### -param Bounds [in]

Vector that determines the bounds.


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
<pre>XMVECTOR Control;

Control.x = (V.x &lt;= Bounds.x &amp;&amp; V.x &gt;= -Bounds.x) ? 0xFFFFFFFF : 0;
Control.y = (V.y &lt;= Bounds.y &amp;&amp; V.y &gt;= -Bounds.y) ? 0xFFFFFFFF : 0;
Control.z = (V.z &lt;= Bounds.z &amp;&amp; V.z &gt;= -Bounds.z) ? 0xFFFFFFFF : 0;
Control.w = (V.w &lt;= Bounds.w &amp;&amp; V.w &gt;= -Bounds.w) ? 0xFFFFFFFF : 0;

return Control;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/7c941454-7410-f3fb-d750-9007f672ed8c">Geometric Vector Functions</a>



<a href="https://msdn.microsoft.com/a55a4fb4-ff6c-4b50-bc14-9e43c4c1683f">XMVectorInBoundsR</a>
 

 

