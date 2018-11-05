---
UID: NN:d3d9.IDirect3DResource9
title: IDirect3DResource9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DResource9 interface to query and prepare resources.
old-location: direct3d9\idirect3dresource9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
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
<a href="https://msdn.microsoft.com/3a7b3faa-ebb6-4b9a-b287-d54394448ca0">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/396921c6-acf4-4dc8-bfc7-e0d5340cb074">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43a83c76-de5e-495d-ad40-023147491f3c">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority for this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7aec1ed-8389-4ea1-9b4f-96f8ed87fddf">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data associated with the resource to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4126cd36-34e5-4224-8b62-54b090322ddc">GetType</a>
</td>
<td align="left" width="63%">
Returns the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c64dc212-06b4-4a81-ab5f-42cde0f29162">PreLoad</a>
</td>
<td align="left" width="63%">
Preloads a managed resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c5b5e86-a0f4-42be-a082-ea645faaa6b3">SetPriority</a>
</td>
<td align="left" width="63%">
Assigns the priority of a resource for scheduling purposes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcd7c261-00a4-41f7-95d3-1076fe986b61">SetPrivateData</a>
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
<a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">IDirect3DDevice9::CreateCubeTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">IDirect3DDevice9::CreateTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">IDirect3DDevice9::CreateVolumeTexture</a>
</li>
</ul>
To create a geometry-oriented resource, you can call one of the following methods.

<ul>
<li>
<a href="https://msdn.microsoft.com/8bfc9f23-ea7a-411b-82b9-5f19cb2f81e0">IDirect3DDevice9::CreateIndexBuffer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">IDirect3DDevice9::CreateVertexBuffer</a>
</li>
</ul>
This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DRESOURCE9 and PDIRECT3DRESOURCE9 types are defined as pointers to the <b>IDirect3DResource9</b> interface. 


    


```

    typedef struct IDirect3DResource9 *LPDIRECT3DRESOURCE9, *PDIRECT3DRESOURCE9;

```





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/815a330c-9fd2-45ff-b7df-192fc197074f">Direct3D Resources (Direct3D 9)</a>
 

 

