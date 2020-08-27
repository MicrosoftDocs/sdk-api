---
UID: NN:d3d9helper.IDirect3DVertexBuffer9
title: IDirect3DVertexBuffer9 (d3d9helper.h)
description: Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources.
helpviewer_keywords: ["618275d7-1a22-b2cf-581b-9cf2495dc642","IDirect3DVertexBuffer9","IDirect3DVertexBuffer9 interface [Direct3D 9]","IDirect3DVertexBuffer9 interface [Direct3D 9]","described","d3d9helper/IDirect3DVertexBuffer9","direct3d9.idirect3dvertexbuffer9"]
old-location: direct3d9\idirect3dvertexbuffer9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexbuffer9.htm
ms.date: 12/05/2018
ms.keywords: 618275d7-1a22-b2cf-581b-9cf2495dc642, IDirect3DVertexBuffer9, IDirect3DVertexBuffer9 interface [Direct3D 9], IDirect3DVertexBuffer9 interface [Direct3D 9],described, d3d9helper/IDirect3DVertexBuffer9, direct3d9.idirect3dvertexbuffer9
f1_keywords:
- d3d9helper/IDirect3DVertexBuffer9
dev_langs:
- c++
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
- IDirect3DVertexBuffer9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVertexBuffer9 interface


## -description


Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVertexBuffer9</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DVertexBuffer9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the vertex buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock">Lock</a>
</td>
<td align="left" width="63%">
Locks a range of vertex data and obtains a pointer to the vertex buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks vertex data.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVertexBuffer9</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a> method.

This interface inherits additional functionality from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVERTEXBUFFER9 and PDIRECT3DVERTEXBUFFER9 types are defined as pointers to the <b>IDirect3DVertexBuffer9</b> interface.
    

    


```

typedef struct IDirect3DVertexBuffer9 *LPDIRECT3DVERTEXBUFFER9, *PDIRECT3DVERTEXBUFFER9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
 

 

