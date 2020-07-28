---
UID: NN:d3d9.IDirect3DIndexBuffer9
title: IDirect3DIndexBuffer9 (d3d9.h)
description: Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource.
helpviewer_keywords: ["IDirect3DIndexBuffer9","IDirect3DIndexBuffer9 interface [Direct3D 9]","IDirect3DIndexBuffer9 interface [Direct3D 9]","described","bb9d32d9-1059-d4c2-6c8c-e4d5a1170082","d3d9helper/IDirect3DIndexBuffer9","direct3d9.idirect3dindexbuffer9"]
old-location: direct3d9\idirect3dindexbuffer9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9.htm
ms.date: 12/05/2018
ms.keywords: IDirect3DIndexBuffer9, IDirect3DIndexBuffer9 interface [Direct3D 9], IDirect3DIndexBuffer9 interface [Direct3D 9],described, bb9d32d9-1059-d4c2-6c8c-e4d5a1170082, d3d9helper/IDirect3DIndexBuffer9, direct3d9.idirect3dindexbuffer9
f1_keywords:
- d3d9/IDirect3DIndexBuffer9
dev_langs:
- c++
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
- IDirect3DIndexBuffer9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DIndexBuffer9 interface


## -description


Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DIndexBuffer9</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DIndexBuffer9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DIndexBuffer9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the index buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock">Lock</a>
</td>
<td align="left" width="63%">
Locks a range of index data and obtains a pointer to the index buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks index data.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DIndexBuffer9</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a> method.

This interface inherits additional functionality from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DINDEXBUFFER9 and PDIRECT3DINDEXBUFFER9 types are defined as pointers to the <b>IDirect3DIndexBuffer9</b> interface. 


```

typedef struct IDirect3DIndexBuffer9 *LPDIRECT3DINDEXBUFFER9, *PDIRECT3DINDEXBUFFER9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
 

 

