---
UID: NF:d3d9.IDirect3DIndexBuffer9.GetDesc
title: IDirect3DIndexBuffer9::GetDesc
author: windows-sdk-content
description: Retrieves a description of the index buffer resource.
old-location: direct3d9\idirect3dindexbuffer9__getdesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9__getdesc.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DIndexBuffer9 interface, IDirect3DIndexBuffer9 interface [Direct3D 9],GetDesc method, IDirect3DIndexBuffer9.GetDesc, IDirect3DIndexBuffer9::GetDesc, d3d9helper/IDirect3DIndexBuffer9::GetDesc, direct3d9.idirect3dindexbuffer9__getdesc, f6d3661c-7957-0918-0367-c148e854bf9f
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DIndexBuffer9.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DIndexBuffer9::GetDesc


## -description


Retrieves a description of the index buffer resource.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172563(v=VS.85).aspx">D3DINDEXBUFFER_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172563(v=VS.85).aspx">D3DINDEXBUFFER_DESC</a> structure, describing the returned index buffer. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174595(v=VS.85).aspx">Index Buffers (Direct3D 9)</a>
 

 

