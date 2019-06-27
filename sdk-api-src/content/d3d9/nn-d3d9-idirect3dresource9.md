---
UID: NN:d3d9.IDirect3DResource9
title: IDirect3DResource9 (d3d9.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DResource9 interface to query and prepare resources.
old-location: direct3d9\idirect3dresource9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3DResource9, IDirect3DResource9 interface [Direct3D 9], IDirect3DResource9 interface [Direct3D 9],described, c545e88d-de95-aa8d-c5e1-4a5285f02095, d3d9helper/IDirect3DResource9, direct3d9.idirect3dresource9
ms.topic: interface
f1_keywords: 
 - "d3d9/IDirect3DResource9"
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DResource9 interface


## -description


Applications use the methods of the <b>IDirect3DResource9</b> interface to query and prepare resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DResource9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DResource9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-freeprivatedata">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-getpriority">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority for this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data associated with the resource to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype">GetType</a>
</td>
<td align="left" width="63%">
Returns the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-preload">PreLoad</a>
</td>
<td align="left" width="63%">
Preloads a managed resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority">SetPriority</a>
</td>
<td align="left" width="63%">
Assigns the priority of a resource for scheduling purposes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setprivatedata">SetPrivateData</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">IDirect3DDevice9::CreateTexture</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">IDirect3DDevice9::CreateVolumeTexture</a>
</li>
</ul>
To create a geometry-oriented resource, you can call one of the following methods.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>
</li>
</ul>
This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DRESOURCE9 and PDIRECT3DRESOURCE9 types are defined as pointers to the <b>IDirect3DResource9</b> interface. 


    


```

    typedef struct IDirect3DResource9 *LPDIRECT3DRESOURCE9, *PDIRECT3DRESOURCE9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/direct3d-resources">Direct3D Resources (Direct3D 9)</a>
 

 

