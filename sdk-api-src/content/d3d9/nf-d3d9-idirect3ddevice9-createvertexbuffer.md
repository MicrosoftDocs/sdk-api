---
UID: NF:d3d9.IDirect3DDevice9.CreateVertexBuffer
title: IDirect3DDevice9::CreateVertexBuffer method
author: windows-driver-content
description: Creates a vertex buffer.
old-location: direct3d9\idirect3ddevice9__createvertexbuffer.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvertexbuffer.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: CreateVertexBuffer method [Direct3D 9], CreateVertexBuffer method [Direct3D 9], IDirect3DDevice9 interface, CreateVertexBuffer,IDirect3DDevice9.CreateVertexBuffer, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], CreateVertexBuffer method, IDirect3DDevice9::CreateVertexBuffer, d3d9helper/IDirect3DDevice9::CreateVertexBuffer, direct3d9.idirect3ddevice9__createvertexbuffer, f6027373-8860-696b-558e-21f53073f7c8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.CreateVertexBuffer
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::CreateVertexBuffer method


## -description


Creates a vertex buffer.


## -parameters




### -param Length [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the vertex buffer, in bytes. For FVF vertex buffers, Length must be large enough to contain at least one vertex, but it need not be a multiple of the vertex size. Length is not validated for non-FVF buffers. See Remarks. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateVertexBuffer with the behavior flags in <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>. For more information, see Remarks. 


### -param FVF [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of <a href="https://msdn.microsoft.com/85d9f5b2-8e4a-4f92-a587-eae5b293778c">D3DFVF</a>, a usage specifier that describes the vertex format of the vertices in this buffer. If this parameter is set to a valid FVF code, the created vertex buffer is an FVF vertex buffer (see Remarks). Otherwise, if this parameter is set to zero, the vertex buffer is a non-FVF vertex buffer. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, describing a valid memory class into which to place the resource. Do not set to D3DPOOL_SCRATCH.


### -param ppVertexBuffer [out, retval]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a> interface, representing the created vertex buffer resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



A vertex buffer can be used with either hardware or software vertex processing. This is determined by how the device and the vertex buffer are created.

When a device is created, CreateDevice uses the behavior flag to determine whether to process vertices in hardware or software. There are three possibilities:

<ul>
<li>Process vertices in hardware by setting D3DCREATE_HARDWARE_VERTEXPROCESSING.</li>
<li>Process vertices in software by setting D3DCREATE_SOFTWARE_VERTEXPROCESSING.</li>
<li>Process vertices in either hardware or software by setting D3DCREATE_MIXED_VERTEXPROCESSING.</li>
</ul>
Mixed-mode devices might need to switch between software and hardware processing (using <a href="https://msdn.microsoft.com/05e67ec5-98f8-47c4-b5b7-aabb974db88a">IDirect3DDevice9::SetSoftwareVertexProcessing</a>) after the device is created.   
    
    
    

When a vertex buffer is created, CreateVertexBuffer uses the usage parameter to decide whether to process vertices in hardware or software.

<ul>
<li>If CreateDevice uses D3DCREATE_HARDWARE_VERTEXPROCESSING, CreateVertexBuffer must use 0.</li>
<li>If CreateDevice uses D3DCREATE_SOFTWARE_VERTEXPROCESSING, CreateVertexBuffer must use either 0 or D3DUSAGE_SOFTWAREPROCESSING. For either value, vertices will be processed in software.</li>
<li>If CreateDevice uses D3DCREATE_MIXED_VERTEXPROCESSING, CreateVertexBuffer can use either 0 or D3DUSAGE_SOFTWAREPROCESSING.</li>
</ul>
To use a vertex buffer with a mixed mode device, create a single vertex buffer which can be used for both hardware or software processing. Use <a href="https://msdn.microsoft.com/15f4cbf8-7f14-4905-b32e-ed253bc0a3de">IDirect3DDevice9::SetStreamSource</a> to set the current vertex buffer and use <a href="https://msdn.microsoft.com/65738aae-aa90-48c5-8c9c-1927d1c92c54">IDirect3DDevice9::SetRenderState</a>, if necessary, to change the device behavior to match. It is recommended that the vertex buffer usage matches the device behavior. Note that a vertex buffer created for software processing cannot be located in video memory.

The <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface supports rendering of primitives using vertex data stored in vertex buffer objects. Vertex buffers are created from the IDirect3DDevice9, and are usable only with the IDirect3DDevice9 object from which they are created.

When set to a nonzero value, which must be a valid FVF code, the FVF parameter indicates that the buffer content is to be characterized by an FVF code. A vertex buffer that is created with an FVF code is referred to as an FVF vertex buffer. For more information, see <a href="https://msdn.microsoft.com/7cab559f-3e9d-46bd-b00f-439e0922aeeb">FVF Vertex Buffers (Direct3D 9)</a>. 

Non-FVF buffers can be used to interleave data during multipass rendering or multitexture rendering in a single pass. To do this, one buffer contains geometry data and the others contain texture coordinates for each texture to be rendered. When rendering, the buffer containing the geometry data is interleaved with each of the buffers containing the texture coordinates. If FVF buffers were used instead, each of them would need to contain identical geometry data in addition to the texture coordinate data specific to each texture rendered. This would result in either a speed or memory penalty, depending on the strategy used. For more information about texture coordinates, see <a href="https://msdn.microsoft.com/184df689-4457-4a2b-88fe-280d8d3f1adb">Texture Coordinates (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/0a34ecb6-6437-46dc-aa79-bf4d24395a86">IDirect3DDevice9::ProcessVertices</a>



<a href="https://msdn.microsoft.com/1f5842e9-b0ea-460c-998a-24ec024bc561">IDirect3DVertexBuffer9::GetDesc</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

