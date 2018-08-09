---
UID: NF:d3d9helper.IDirect3DDevice9.ProcessVertices
title: IDirect3DDevice9::ProcessVertices
author: windows-sdk-content
description: Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer.
old-location: direct3d9\idirect3ddevice9__processvertices.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__processvertices.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],ProcessVertices method, IDirect3DDevice9.ProcessVertices, IDirect3DDevice9::ProcessVertices, ProcessVertices, ProcessVertices method [Direct3D 9], ProcessVertices method [Direct3D 9],IDirect3DDevice9 interface, cf036375-2448-6e34-11ef-e3e3b96c951f, d3d9helper/IDirect3DDevice9::ProcessVertices, direct3d9.idirect3ddevice9__processvertices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.ProcessVertices
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::ProcessVertices


## -description


Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. 


## -parameters




### -param SrcStartIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of first vertex to load. 


### -param DestIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of first vertex in the destination vertex buffer into which the results are placed. 


### -param VertexCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices to process. 


### -param pDestBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a> interface, the destination vertex buffer representing the stream of interleaved vertex data. 


### -param pVertexDecl [in]

Type: <b><a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a> interface that represents the output vertex data declaration. When vertex shader 3.0 or above is set as the current vertex shader, the output vertex declaration must be present.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Processing options. Set this parameter to 0 for default processing. Set to D3DPV_DONOTCOPYDATA to prevent the system from copying vertex data not affected by the vertex operation into the destination buffer. The D3DPV_DONOTCOPYDATA value may be combined with one or more <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK</a> values appropriate for the destination buffer.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



The order of operations for this method is as follows:

<ul>
<li>Transform vertices to projection space using the world + view + projection matrix.</li>
<li>Compute screen coordinates using viewport settings.</li>
<li>If clipping is enabled, compute clipping codes and store them in an internal buffer, associated with the destination vertex buffer. If a vertex is inside the viewing frustum, its screen coordinates are computed. If the vertex is outside the viewing frustum, the vertex is stored in the destination vertex buffer in projection space coordinates.</li>
<li>Other notes: The user does not have access to the internal clip code buffer. No clipping is done on triangles or any other primitives.</li>
</ul>
The destination vertex buffer, pDestBuffer, must be created with a nonzero FVF parameter in <a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">IDirect3DDevice9::CreateVertexBuffer</a>. The FVF code specified during the call to the <b>IDirect3DDevice9::CreateVertexBuffer</b> method specifies the vertex elements present in the destination vertex buffer.

When Direct3D generates texture coordinates, or copies or transforms input texture coordinates, and the output texture coordinate format defines more texture coordinate components than Direct3D generates, Direct3D does not change these extra components.




## -see-also




<a href="https://msdn.microsoft.com/4f9ca83d-c9d6-4749-944d-78f831b0f44e">Device Types and Vertex Processing Requirements (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/a882a5c5-b05e-4659-9040-92d3e2ccd89c">Fixed Function Vertex Processing (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

