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

# IDirect3DDevice9::CreateVertexDeclaration


## -description


Create a vertex shader declaration from the device and the vertex elements.


## -parameters




### -param pVertexElements [in]

Type: <b>const <a href="https://msdn.microsoft.com/6f3c40a0-b28e-48d6-acad-ef80a919c5d7">D3DVERTEXELEMENT9</a>*</b>

An array of <a href="https://msdn.microsoft.com/6f3c40a0-b28e-48d6-acad-ef80a919c5d7">D3DVERTEXELEMENT9</a> vertex elements.


### -param ppDecl [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/3c4a18a5-5307-48d0-8a21-afb343d5d816">IDirect3DVertexDeclaration9</a> pointer that returns the created vertex shader declaration.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -remarks



See the <a href="https://msdn.microsoft.com/09dae498-3b33-4c33-bc7e-47f2bf784e4c">Vertex Declaration (Direct3D 9)</a> page for a detailed description of how to map vertex declarations between different versions of DirectX.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

