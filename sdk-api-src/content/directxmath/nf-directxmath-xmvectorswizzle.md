---
UID: NF:directxmath.XMVectorSwizzle
title: XMVectorSwizzle function
author: windows-sdk-content
description: Swizzles a vector.
old-location: dxmath\xmvectorswizzle.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorSwizzle(XMVECTOR,uint32_t,uint32_t,uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorSwizzle, XMVectorSwizzle, XMVectorSwizzle method [DirectX Math Support APIs], dxmath.xmvectorswizzle
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
 - XMVectorSwizzle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorSwizzle function


## -description


Swizzles a vector.


## -parameters




### -param V [in]

Vector to swizzle.


### -param E0 [in]

Index that describes which component of <i>V</i> to place in the x-component of the swizzled vector. A value of 0
        selects the x-component, 1 selects the y-component, 2 selects the z-component, and 3 selects the w-component.


### -param E1 [in]

Index that describes which component of <i>V</i> to place in the y-component of the swizzled vector. A value of 0
        selects the x-component, 1 selects the y-component, 2 selects the z-component, and 3 selects the w-component.


### -param E2 [in]

Index that describes which component of <i>V</i> to place in the z-component of the swizzled vector. A value of 0
        selects the x-component, 1 selects the y-component, 2 selects the z-component, and 3 selects the w-component.


### -param E3 [in]

Index that describes which component of <i>V</i> to place in the w-component of the swizzled vector. A value of 0
        selects the x-component, 1 selects the y-component, 2 selects the z-component, and 3 selects the w-component.


## -returns



Returns the swizzled <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.




## -remarks



The following code demonstrates how this function might be used.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR v = XMVectorSet( 10.0f, 20.0f, 30.0f, 40.0f );
XMVECTOR result = XMVectorSwizzle(v, 3, 3, 0, 2 );</pre>
</td>
</tr>
</table></span></div>
The swizzled vector (<i>result</i>) will be &lt;40.0f, 40.0f, 10.0f, 30.0f&gt;.

<code>XM_SWIZZLE_X</code>, <code>XM_SWIZZLE_Y</code>, <code>XM_SWIZZLE_Z</code>, and <code>XM_SWIZZLE_W</code> are constants which 
   evaluate to 0, 1, 2, and 3 respectively for use with <b>XMVectorSwizzle</b>. 
   This is identical to <code>XM_PERMUTE_0X</code>, <code>XM_PERMUTE_0Y</code>, <code>XM_PERMUTE_0Z</code>, and <code>XM_PERMUTE_0W</code>.

For the case of constant indices (E0, E1, E2, E3), it is much more efficent to use the template form of <a href="https://msdn.microsoft.com/75608e80-5911-45a8-beca-ceac1f4d2c1c">XMVectorSwizzle</a>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
template&lt;uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW&gt;
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

Example: XMVectorSwizzle&lt; 3, 3, 0, 2&gt;(v);
   </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f5464614-f6bb-427d-5488-3ba0fd4c6e8d">Component-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/212c9381-6bde-4a09-9710-e2e3fe54f405">XMVectorPermute</a>
 

 

