---
UID: NF:d3d9helper.IDirect3DVertexBuffer9.GetDesc
title: IDirect3DVertexBuffer9::GetDesc
author: windows-sdk-content
description: Retrieves a description of the vertex buffer resource.
old-location: direct3d9\idirect3dvertexbuffer9__getdesc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexbuffer9__getdesc.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 757c012d-2bd8-4555-34bc-493f1a96904f, GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DVertexBuffer9 interface, IDirect3DVertexBuffer9 interface [Direct3D 9],GetDesc method, IDirect3DVertexBuffer9.GetDesc, IDirect3DVertexBuffer9::GetDesc, d3d9helper/IDirect3DVertexBuffer9::GetDesc, direct3d9.idirect3dvertexbuffer9__getdesc
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
 - IDirect3DVertexBuffer9.GetDesc
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVertexBuffer9::GetDesc


## -description


Retrieves a description of the vertex buffer resource.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/0ae8f976-d0ca-4d55-b6db-5be85fa3c799">D3DVERTEXBUFFER_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/0ae8f976-d0ca-4d55-b6db-5be85fa3c799">D3DVERTEXBUFFER_DESC</a> structure, describing the returned vertex buffer. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

