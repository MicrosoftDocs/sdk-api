---
UID: NF:d3d9helper.IDirect3DDevice9.CreateVertexBuffer
title: IDirect3DDevice9::CreateVertexBuffer (d3d9helper.h)
description: The IDirect3DDevice9::CreateVertexBuffer method (d3d9helper.h) creates a vertex buffer.
helpviewer_keywords: ["CreateVertexBuffer","CreateVertexBuffer method [Direct3D 9]","CreateVertexBuffer method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateVertexBuffer method","IDirect3DDevice9.CreateVertexBuffer","IDirect3DDevice9::CreateVertexBuffer","d3d9helper/IDirect3DDevice9::CreateVertexBuffer","direct3d9.idirect3ddevice9__createvertexbuffer","f6027373-8860-696b-558e-21f53073f7c8"]
old-location: direct3d9\idirect3ddevice9__createvertexbuffer.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvertexbuffer.htm
ms.date: 08/11/2022
ms.keywords: CreateVertexBuffer, CreateVertexBuffer method [Direct3D 9], CreateVertexBuffer method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVertexBuffer method, IDirect3DDevice9.CreateVertexBuffer, IDirect3DDevice9::CreateVertexBuffer, d3d9helper/IDirect3DDevice9::CreateVertexBuffer, direct3d9.idirect3ddevice9__createvertexbuffer, f6027373-8860-696b-558e-21f53073f7c8
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::CreateVertexBuffer
 - d3d9helper/IDirect3DDevice9::CreateVertexBuffer
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
 - IDirect3DDevice9.CreateVertexBuffer
---

# IDirect3DDevice9::CreateVertexBuffer


## -description

Creates a vertex buffer.

## -parameters

### -param Length [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the vertex buffer, in bytes. For FVF vertex buffers, Length must be large enough to contain at least one vertex, but it need not be a multiple of the vertex size. Length is not validated for non-FVF buffers. See Remarks.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateVertexBuffer with the behavior flags in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>. For more information, see Remarks.

### -param FVF [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of <a href="/windows/desktop/direct3d9/d3dfvf">D3DFVF</a>, a usage specifier that describes the vertex format of the vertices in this buffer. If this parameter is set to a valid FVF code, the created vertex buffer is an FVF vertex buffer (see Remarks). Otherwise, if this parameter is set to zero, the vertex buffer is a non-FVF vertex buffer.

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a> enumerated type, describing a valid memory class into which to place the resource. Do not set to D3DPOOL_SCRATCH.

### -param ppVertexBuffer [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a> interface, representing the created vertex buffer resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

A vertex buffer can be used with either hardware or software vertex processing. This is determined by how the device and the vertex buffer are created.

When a device is created, CreateDevice uses the behavior flag to determine whether to process vertices in hardware or software. There are three possibilities:

<ul>
<li>Process vertices in hardware by setting D3DCREATE_HARDWARE_VERTEXPROCESSING.</li>
<li>Process vertices in software by setting D3DCREATE_SOFTWARE_VERTEXPROCESSING.</li>
<li>Process vertices in either hardware or software by setting D3DCREATE_MIXED_VERTEXPROCESSING.</li>
</ul>
Mixed-mode devices might need to switch between software and hardware processing (using <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing">IDirect3DDevice9::SetSoftwareVertexProcessing</a>) after the device is created.   
    
    
    

When a vertex buffer is created, CreateVertexBuffer uses the usage parameter to decide whether to process vertices in hardware or software.

<ul>
<li>If CreateDevice uses D3DCREATE_HARDWARE_VERTEXPROCESSING, CreateVertexBuffer must use 0.</li>
<li>If CreateDevice uses D3DCREATE_SOFTWARE_VERTEXPROCESSING, CreateVertexBuffer must use either 0 or D3DUSAGE_SOFTWAREPROCESSING. For either value, vertices will be processed in software.</li>
<li>If CreateDevice uses D3DCREATE_MIXED_VERTEXPROCESSING, CreateVertexBuffer can use either 0 or D3DUSAGE_SOFTWAREPROCESSING.</li>
</ul>
To use a vertex buffer with a mixed mode device, create a single vertex buffer which can be used for both hardware or software processing. Use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource">IDirect3DDevice9::SetStreamSource</a> to set the current vertex buffer and use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">IDirect3DDevice9::SetRenderState</a>, if necessary, to change the device behavior to match. It is recommended that the vertex buffer usage matches the device behavior. Note that a vertex buffer created for software processing cannot be located in video memory.

The <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface supports rendering of primitives using vertex data stored in vertex buffer objects. Vertex buffers are created from the IDirect3DDevice9, and are usable only with the IDirect3DDevice9 object from which they are created.

When set to a nonzero value, which must be a valid FVF code, the FVF parameter indicates that the buffer content is to be characterized by an FVF code. A vertex buffer that is created with an FVF code is referred to as an FVF vertex buffer. For more information, see <a href="/windows/desktop/direct3d9/fvf-vertex-buffers">FVF Vertex Buffers (Direct3D 9)</a>. 

Non-FVF buffers can be used to interleave data during multipass rendering or multitexture rendering in a single pass. To do this, one buffer contains geometry data and the others contain texture coordinates for each texture to be rendered. When rendering, the buffer containing the geometry data is interleaved with each of the buffers containing the texture coordinates. If FVF buffers were used instead, each of them would need to contain identical geometry data in addition to the texture coordinate data specific to each texture rendered. This would result in either a speed or memory penalty, depending on the strategy used. For more information about texture coordinates, see <a href="/windows/desktop/direct3d9/texture-coordinates">Texture Coordinates (Direct3D 9)</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-processvertices">IDirect3DDevice9::ProcessVertices</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc">IDirect3DVertexBuffer9::GetDesc</a>



<a href="/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
