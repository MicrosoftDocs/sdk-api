---
UID: NN:d3d9helper.IDirect3DVertexBuffer9
title: IDirect3DVertexBuffer9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources.
old-location: direct3d9\idirect3dvertexbuffer9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexbuffer9.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 618275d7-1a22-b2cf-581b-9cf2495dc642, IDirect3DVertexBuffer9, IDirect3DVertexBuffer9 interface [Direct3D 9], IDirect3DVertexBuffer9 interface [Direct3D 9],described, d3d9helper/IDirect3DVertexBuffer9, direct3d9.idirect3dvertexbuffer9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9helper.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DVertexBuffer9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DVertexBuffer9 interface


## -description


Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVertexBuffer9</b> interface inherits from <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>. <b>IDirect3DVertexBuffer9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVertexBuffer9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f5842e9-b0ea-460c-998a-24ec024bc561">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the vertex buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d967ea07-a59f-401a-a63a-a1a764f91485">Lock</a>
</td>
<td align="left" width="63%">
Locks a range of vertex data and obtains a pointer to the vertex buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72932c97-d515-4f50-94ec-274274248cd4">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks vertex data.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVertexBuffer9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">IDirect3DDevice9::CreateVertexBuffer</a> method.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DVERTEXBUFFER9 and PDIRECT3DVERTEXBUFFER9 types are defined as pointers to the <b>IDirect3DVertexBuffer9</b> interface.
    

    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DVertexBuffer9 *LPDIRECT3DVERTEXBUFFER9, *PDIRECT3DVERTEXBUFFER9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">IDirect3DDevice9::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

