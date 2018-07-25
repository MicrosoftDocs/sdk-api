---
UID: NN:d3d9.IDirect3DResource9
title: IDirect3DResource9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DResource9 interface to query and prepare resources.
old-location: direct3d9\idirect3dresource9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IDirect3DResource9, IDirect3DResource9 interface [Direct3D 9], IDirect3DResource9 interface [Direct3D 9],described, c545e88d-de95-aa8d-c5e1-4a5285f02095, d3d9helper/IDirect3DResource9, direct3d9.idirect3dresource9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DResource9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DResource9 interface


## -description


Applications use the methods of the <b>IDirect3DResource9</b> interface to query and prepare resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DResource9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DResource9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DResource9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205879(v=VS.85).aspx">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205881(v=VS.85).aspx">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority for this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205882(v=VS.85).aspx">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data associated with the resource to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Returns the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205884(v=VS.85).aspx">PreLoad</a>
</td>
<td align="left" width="63%">
Preloads a managed resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205885(v=VS.85).aspx">SetPriority</a>
</td>
<td align="left" width="63%">
Assigns the priority of a resource for scheduling purposes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205886(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource.

</td>
</tr>
</table> 


## -remarks



To create a texture resource, you can call one of the following methods.

<ul>
<li>
<a href="https://msdn.microsoft.com/library/Bb174355(v=VS.85).aspx">IDirect3DDevice9::CreateCubeTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb174363(v=VS.85).aspx">IDirect3DDevice9::CreateTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb174367(v=VS.85).aspx">IDirect3DDevice9::CreateVolumeTexture</a>
</li>
</ul>
To create a geometry-oriented resource, you can call one of the following methods.

<ul>
<li>
<a href="https://msdn.microsoft.com/library/Bb174357(v=VS.85).aspx">IDirect3DDevice9::CreateIndexBuffer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb174364(v=VS.85).aspx">IDirect3DDevice9::CreateVertexBuffer</a>
</li>
</ul>
This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DRESOURCE9 and PDIRECT3DRESOURCE9 types are defined as pointers to the <b>IDirect3DResource9</b> interface. 


    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    typedef struct IDirect3DResource9 *LPDIRECT3DRESOURCE9, *PDIRECT3DRESOURCE9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb219682(v=VS.85).aspx">Direct3D Resources (Direct3D 9)</a>
 

 

