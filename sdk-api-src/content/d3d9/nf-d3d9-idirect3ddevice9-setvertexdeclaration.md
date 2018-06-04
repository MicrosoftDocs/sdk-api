---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

