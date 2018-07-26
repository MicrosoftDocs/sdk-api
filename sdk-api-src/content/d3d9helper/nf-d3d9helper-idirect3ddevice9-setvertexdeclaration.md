---
UID: NF:d3d9helper.IDirect3DDevice9.SetVertexDeclaration
title: IDirect3DDevice9::SetVertexDeclaration
author: windows-sdk-content
description: Sets a Vertex Declaration (Direct3D 9).
old-location: direct3d9\idirect3ddevice9__setvertexdeclaration.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexdeclaration.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 12796c02-d1b4-5f9d-8414-04b978887c2a, IDirect3DDevice9 interface [Direct3D 9],SetVertexDeclaration method, IDirect3DDevice9.SetVertexDeclaration, IDirect3DDevice9::SetVertexDeclaration, SetVertexDeclaration, SetVertexDeclaration method [Direct3D 9], SetVertexDeclaration method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetVertexDeclaration, direct3d9.idirect3ddevice9__setvertexdeclaration
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
 - IDirect3DDevice9.SetVertexDeclaration
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetVertexDeclaration


## -description


Sets a <a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a>.


## -parameters




### -param pDecl [in]

Type: <b><a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a> object, which contains the vertex declaration.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 The return value can be D3DERR_INVALIDCALL.




## -remarks



A vertex declaration is an IDirect3DVertexDeclaration9 object that defines the data members of a vertex (i.e. texture coordinates, colors, normals, etc.). This data can be useful for implementing <a href="https://msdn.microsoft.com/4894e085-30e7-4cc5-8ae6-a84b601e4ce3">vertex shaders and pixel shaders</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/842f8b2f-cdfd-4d88-a114-7b129f09fd61">IDirect3DDevice9::GetVertexDeclaration</a>
 

 

