---
UID: NN:d3d9helper.IDirect3DIndexBuffer9
title: IDirect3DIndexBuffer9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource.
old-location: direct3d9\idirect3dindexbuffer9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DIndexBuffer9, IDirect3DIndexBuffer9 interface [Direct3D 9], IDirect3DIndexBuffer9 interface [Direct3D 9],described, bb9d32d9-1059-d4c2-6c8c-e4d5a1170082, d3d9helper/IDirect3DIndexBuffer9, direct3d9.idirect3dindexbuffer9
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
 - IDirect3DIndexBuffer9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DIndexBuffer9 interface


## -description


Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DIndexBuffer9</b> interface inherits from <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>. <b>IDirect3DIndexBuffer9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/33c33c28-b57a-4e52-a29b-9117bd60460b">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the index buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7fa912c-d31b-452a-b1ec-c19025b0daeb">Lock</a>
</td>
<td align="left" width="63%">
Locks a range of index data and obtains a pointer to the index buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/545e2f9f-01dc-4121-9888-bcab7d25b459">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks index data.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DIndexBuffer9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/8bfc9f23-ea7a-411b-82b9-5f19cb2f81e0">IDirect3DDevice9::CreateIndexBuffer</a> method.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DINDEXBUFFER9 and PDIRECT3DINDEXBUFFER9 types are defined as pointers to the <b>IDirect3DIndexBuffer9</b> interface. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DIndexBuffer9 *LPDIRECT3DINDEXBUFFER9, *PDIRECT3DINDEXBUFFER9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/8bfc9f23-ea7a-411b-82b9-5f19cb2f81e0">IDirect3DDevice9::CreateIndexBuffer</a>



<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>



<a href="https://msdn.microsoft.com/baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784">Index Buffers (Direct3D 9)</a>
 

 

