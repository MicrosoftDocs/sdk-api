---
UID: NF:d3d9.IDirect3DDevice9.CreateIndexBuffer
title: IDirect3DDevice9::CreateIndexBuffer (d3d9.h)
description: The IDirect3DDevice9::CreateIndexBuffer method (d3d9.h) creates an index buffer. 
helpviewer_keywords: ["532a9cb1-de3a-0873-68d0-511852df653f","CreateIndexBuffer","CreateIndexBuffer method [Direct3D 9]","CreateIndexBuffer method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateIndexBuffer method","IDirect3DDevice9.CreateIndexBuffer","IDirect3DDevice9::CreateIndexBuffer","d3d9helper/IDirect3DDevice9::CreateIndexBuffer","direct3d9.idirect3ddevice9__createindexbuffer"]
old-location: direct3d9\idirect3ddevice9__createindexbuffer.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createindexbuffer.htm
ms.date: 08/10/2022
ms.keywords: 532a9cb1-de3a-0873-68d0-511852df653f, CreateIndexBuffer, CreateIndexBuffer method [Direct3D 9], CreateIndexBuffer method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateIndexBuffer method, IDirect3DDevice9.CreateIndexBuffer, IDirect3DDevice9::CreateIndexBuffer, d3d9helper/IDirect3DDevice9::CreateIndexBuffer, direct3d9.idirect3ddevice9__createindexbuffer
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::CreateIndexBuffer
 - d3d9/IDirect3DDevice9::CreateIndexBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.CreateIndexBuffer
---

# IDirect3DDevice9::CreateIndexBuffer


## -description

Creates an index buffer.

## -parameters

### -param Length [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the index buffer, in bytes.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateIndexBuffer with the behavior flags in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>. For more information, see Remarks.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of the index buffer. For more information, see Remarks. The valid settings are the following: 



<table>
<tr>
<th>Item</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="D3DFMT_INDEX16"></a><a id="d3dfmt_index16"></a>D3DFMT_INDEX16

</td>
<td width="60%">
Indices are 16 bits each.

</td>
</tr>
<tr>
<td width="40%">
<a id="D3DFMT_INDEX32"></a><a id="d3dfmt_index32"></a>D3DFMT_INDEX32

</td>
<td width="60%">
Indices are 32 bits each.

</td>
</tr>
</table>

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a> enumerated type, describing a valid memory class into which to place the resource.

### -param ppIndexBuffer [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a> interface, representing the created index buffer resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>; set it to <b>NULL</b> to not share a resource. This parameter is not used in Direct3D 9 for operating systems earlier than Windows Vista; set it to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, D3DXERR_INVALIDDATA, E_OUTOFMEMORY.

## -remarks

Index buffers are memory resources used to hold indices, they are similar to both surfaces and vertex buffers. The use of index buffers enables Direct3D to avoid unnecessary data copying and to place the buffer in the optimal memory type for the expected usage.

To use index buffers, create an index buffer, lock it, fill it with indices, unlock it, pass it to <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setindices">IDirect3DDevice9::SetIndices</a>, set up the vertices, set up the vertex shader, and call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a> for rendering.

The MaxVertexIndex member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure indicates the types of index buffers that are valid for rendering.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc">IDirect3DIndexBuffer9::GetDesc</a>



<a href="/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
