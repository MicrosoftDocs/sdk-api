---
UID: NF:directxmath.XMVectorPermute
title: XMVectorPermute function
author: windows-sdk-content
description: Permutes the components of two vectors to create a new vector.
old-location: dxmath\xmvectorpermute.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorPermute(XMVECTOR,XMVECTOR,unit32_t,unit32_t,unit32_t,unit32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorPermute, XMVectorPermute, XMVectorPermute method [DirectX Math Support APIs], dxmath.xmvectorpermute
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
 - XMVectorPermute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorPermute function


## -description


Permutes the components of two vectors to create a new vector.


## -parameters




### -param V1 [in]

First vector.


### -param V2 [in]

Second vector.


### -param PermuteX

Index form 0-7 indicating where the X component of the new vector should be copied from.


### -param PermuteY

Index form 0-7 indicating where the Y component of the new vector should be copied from.


### -param PermuteZ

Index form 0-7 indicating where the Z component of the new vector should be copied from.


### -param PermuteW

Index form 0-7 indicating where the W component of the new vector should be copied from.


## -returns



Returns the permuted vector that resulted from combining the source vectors.




## -remarks



If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), 
    use <a href="https://msdn.microsoft.com/en-us/library/Hh404826(v=VS.85).aspx">XMVectorSwizzle</a> instead for better performance.

The <a href="https://msdn.microsoft.com/a206fe22-12c8-ac2b-ee37-20cfff35841a">XM_PERMUTE_</a> constants are provided to
    use as input values for <i>PermuteX</i>,<i>PermuteY</i>,<i>PermuteZ</i>, and <i>PermuteW</i>.

For constant PermuteX/Y/Z/W parameters, it is much more efficent to use the template form of
    <a href="https://msdn.microsoft.com/en-us/library/Hh855944(v=VS.85).aspx">XMVectorPermute</a>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

Example: XMVectorPermute<XM_PERMUTE_0Z, XM_PERMUTE_1X, XM_PERMUTE_0W, XM_PERMUTE_1Y>( V1, V2 );
   </pre>
</td>
</tr>
</table></span></div>


<div class="alert"><b>Note</b>  This version of <code>XMVectorPermute</code> is new for DirectXMath.  The XNAMath v2.x library made use of <code>XMVectorPermuteControl</code>, 
     a control <code>XMVECTOR</code> instead of 4 indicies for <code>XMVectorPermute</code>, and used different values for the XM_PERMUTE_x constants.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f5464614-f6bb-427d-5488-3ba0fd4c6e8d">Component-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404826(v=VS.85).aspx">XMVectorSwizzle</a>
 

 

