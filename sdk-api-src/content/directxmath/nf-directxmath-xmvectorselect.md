---
UID: NF:directxmath.XMVectorSelect
title: XMVectorSelect function
author: windows-sdk-content
description: Performs a per-component selection between two input vectors and returns the resulting vector.
old-location: dxmath\xmvectorselect.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorSelect(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVectorSelect, XMVectorSelect, XMVectorSelect method [DirectX Math Support APIs], dxmath.xmvectorselect
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
 - XMVectorSelect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorSelect function


## -description


Performs a per-component selection between two input vectors and returns the resulting vector.


## -parameters




### -param V1 [in]

First vector to compare.


### -param V2 [in]

Second vector to compare.


### -param Control [in]

Vector mask used to select a vector component from either <i>V1</i> or <i>V2</i>. If a component of
        <i>Control</i> is zero, the returned vector's corresponding component will be the first vector's component.
        If a component of <i>Control</i> is 0xFF, the returned vector's corresponding component will be the second
        vector's component. For full details on how the vector mask works, see the "Remarks".

Typically, the vector used for <i>Control</i> will be either the output of a vector comparison function (such as
        <a href="https://msdn.microsoft.com/e5e3d343-6baf-4d98-b303-5d1b12bb285d">XMVectorEqual</a>,
        <a href="https://msdn.microsoft.com/b9923970-cb72-4af3-bd5a-83daba8c59de">XMVectorLess</a>, or
        <a href="https://msdn.microsoft.com/f28155e6-745e-4ed5-ba3b-218f63c18c92">XMVectorGreater</a>) or it will be the output
        of <a href="https://msdn.microsoft.com/307660ea-09d4-49ce-b4ed-4a0e5ad1f021">XMVectorSelectControl</a>.


## -returns



Returns the result of the per-component selection.




## -remarks



If any given bit of <i>Control</i> is set, the corresponding bit from <i>V2</i> is used, otherwise, the
   corresponding bit from <i>V1</i> is used. The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.u[0] = (V1.u[0] &amp; ~Control.u[0]) | (V2.u[0] &amp; Control.u[0]);
Result.u[1] = (V1.u[1] &amp; ~Control.u[1]) | (V2.u[1] &amp; Control.u[1]);
Result.u[2] = (V1.u[2] &amp; ~Control.u[2]) | (V2.u[2] &amp; Control.u[2]);
Result.u[3] = (V1.u[3] &amp; ~Control.u[3]) | (V2.u[3] &amp; Control.u[3]);

return Result;</pre>
</td>
</tr>
</table></span></div>
Manual construction of a control vector is not necessary. There are two simple ways of constructing an appropriate
   control vector:

<ul>
<li>
Using the <a href="https://msdn.microsoft.com/307660ea-09d4-49ce-b4ed-4a0e5ad1f021">XMVectorSelectControl</a>function to construct a control vector.

See <a href="https://msdn.microsoft.com/307660ea-09d4-49ce-b4ed-4a0e5ad1f021">Using XMVectorSelect and
       XMVectorSelectControl</a> for a demonstration of how this function can be used.

</li>
<li>
The control vector can be constructed using the XM_SELECT_[0,1] constant (see
       <a href="https://msdn.microsoft.com/a206fe22-12c8-ac2b-ee37-20cfff35841a">DirectXMath Library Constants</a>). As an example, in pseudo-code, an instance of
       <i>Control</i> with the elements:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>   Control = { XM_SELECT_0,   XM_SELECT_1,   XM_SELECT_0,   XM_SELECT_1 }</pre>
</td>
</tr>
</table></span></div>
would return a vector <i>Result</i> with the following components of <i>V1</i> and <i>V2</i>

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>   Result = { V1.X,  V2.Y,   V1.Z,   V2.W }</pre>
</td>
</tr>
</table></span></div>
</li>
</ul>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f5464614-f6bb-427d-5488-3ba0fd4c6e8d">Component-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/307660ea-09d4-49ce-b4ed-4a0e5ad1f021">XMVectorSelectControl</a>
 

 

