---
UID: NF:d3d9helper.IDirect3DDevice9.ProcessVertices
title: IDirect3DDevice9::ProcessVertices (d3d9helper.h)
description: The IDirect3DDevice9::ProcessVertices method (d3d9.h) applies the vertex processing defined by the vertex shader to the set of input data streams.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","ProcessVertices method","IDirect3DDevice9.ProcessVertices","IDirect3DDevice9::ProcessVertices","ProcessVertices","ProcessVertices method [Direct3D 9]","ProcessVertices method [Direct3D 9]","IDirect3DDevice9 interface","cf036375-2448-6e34-11ef-e3e3b96c951f","d3d9helper/IDirect3DDevice9::ProcessVertices","direct3d9.idirect3ddevice9__processvertices"]
old-location: direct3d9\idirect3ddevice9__processvertices.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__processvertices.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],ProcessVertices method, IDirect3DDevice9.ProcessVertices, IDirect3DDevice9::ProcessVertices, ProcessVertices, ProcessVertices method [Direct3D 9], ProcessVertices method [Direct3D 9],IDirect3DDevice9 interface, cf036375-2448-6e34-11ef-e3e3b96c951f, d3d9helper/IDirect3DDevice9::ProcessVertices, direct3d9.idirect3ddevice9__processvertices
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
 - IDirect3DDevice9::ProcessVertices
 - d3d9helper/IDirect3DDevice9::ProcessVertices
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
 - IDirect3DDevice9.ProcessVertices
---

# IDirect3DDevice9::ProcessVertices


## -description

Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer.

## -parameters

### -param SrcStartIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of first vertex to load.

### -param DestIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of first vertex in the destination vertex buffer into which the results are placed.

### -param VertexCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of vertices to process.

### -param pDestBuffer [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a> interface, the destination vertex buffer representing the stream of interleaved vertex data.

### -param pVertexDecl [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a> interface that represents the output vertex data declaration. When vertex shader 3.0 or above is set as the current vertex shader, the output vertex declaration must be present.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Processing options. Set this parameter to 0 for default processing. Set to D3DPV_DONOTCOPYDATA to prevent the system from copying vertex data not affected by the vertex operation into the destination buffer. The D3DPV_DONOTCOPYDATA value may be combined with one or more <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK</a> values appropriate for the destination buffer.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

The order of operations for this method is as follows:

<ul>
<li>Transform vertices to projection space using the world + view + projection matrix.</li>
<li>Compute screen coordinates using viewport settings.</li>
<li>If clipping is enabled, compute clipping codes and store them in an internal buffer, associated with the destination vertex buffer. If a vertex is inside the viewing frustum, its screen coordinates are computed. If the vertex is outside the viewing frustum, the vertex is stored in the destination vertex buffer in projection space coordinates.</li>
<li>Other notes: The user does not have access to the internal clip code buffer. No clipping is done on triangles or any other primitives.</li>
</ul>
The destination vertex buffer, pDestBuffer, must be created with a nonzero FVF parameter in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>. The FVF code specified during the call to the <b>IDirect3DDevice9::CreateVertexBuffer</b> method specifies the vertex elements present in the destination vertex buffer.

When Direct3D generates texture coordinates, or copies or transforms input texture coordinates, and the output texture coordinate format defines more texture coordinate components than Direct3D generates, Direct3D does not change these extra components.

## -see-also

<a href="/windows/desktop/direct3d9/device-types-and-vertex-processing-requirements">Device Types and Vertex Processing Requirements (Direct3D 9)</a>



<a href="/windows/desktop/direct3d9/fixed-function-vertex-processing">Fixed Function Vertex Processing (Direct3D 9)</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
