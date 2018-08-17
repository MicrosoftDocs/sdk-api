---
UID: NF:d3d9helper.IDirect3DDevice9.CreateIndexBuffer
title: IDirect3DDevice9::CreateIndexBuffer
author: windows-sdk-content
description: Creates an index buffer.
old-location: direct3d9\idirect3ddevice9__createindexbuffer.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createindexbuffer.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 532a9cb1-de3a-0873-68d0-511852df653f, CreateIndexBuffer, CreateIndexBuffer method [Direct3D 9], CreateIndexBuffer method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateIndexBuffer method, IDirect3DDevice9.CreateIndexBuffer, IDirect3DDevice9::CreateIndexBuffer, d3d9helper/IDirect3DDevice9::CreateIndexBuffer, direct3d9.idirect3ddevice9__createindexbuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
 - IDirect3DDevice9.CreateIndexBuffer
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::CreateIndexBuffer


## -description


Creates an index buffer.


## -parameters




### -param Length [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the index buffer, in bytes. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateIndexBuffer with the behavior flags in <a href="https://msdn.microsoft.com/en-us/library/Bb174313(v=VS.85).aspx">IDirect3D9::CreateDevice</a>. For more information, see Remarks. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a> enumerated type, describing the format of the index buffer. For more information, see Remarks. The valid settings are the following: 



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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a> enumerated type, describing a valid memory class into which to place the resource. 


### -param ppIndexBuffer [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a> interface, representing the created index buffer resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/en-us/library/Bb219800(v=VS.85).aspx">share resources</a>; set it to <b>NULL</b> to not share a resource. This parameter is not used in Direct3D 9 for operating systems earlier than Windows Vista; set it to <b>NULL</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, D3DXERR_INVALIDDATA, E_OUTOFMEMORY. 




## -remarks



Index buffers are memory resources used to hold indices, they are similar to both surfaces and vertex buffers. The use of index buffers enables Direct3D to avoid unnecessary data copying and to place the buffer in the optimal memory type for the expected usage.

To use index buffers, create an index buffer, lock it, fill it with indices, unlock it, pass it to <a href="https://msdn.microsoft.com/en-us/library/Bb174435(v=VS.85).aspx">IDirect3DDevice9::SetIndices</a>, set up the vertices, set up the vertex shader, and call <a href="https://msdn.microsoft.com/en-us/library/Bb174369(v=VS.85).aspx">IDirect3DDevice9::DrawIndexedPrimitive</a> for rendering.

The MaxVertexIndex member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure indicates the types of index buffers that are valid for rendering.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205866(v=VS.85).aspx">IDirect3DIndexBuffer9::GetDesc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174595(v=VS.85).aspx">Index Buffers (Direct3D 9)</a>
 

 

