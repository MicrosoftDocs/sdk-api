---
UID: NF:d3d9.IDirect3DDevice9.SetIndices
title: IDirect3DDevice9::SetIndices
author: windows-sdk-content
description: Sets index data.
old-location: direct3d9\idirect3ddevice9__setindices.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setindices.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetIndices method, IDirect3DDevice9.SetIndices, IDirect3DDevice9::SetIndices, SetIndices, SetIndices method [Direct3D 9], SetIndices method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetIndices, direct3d9.idirect3ddevice9__setindices, f1b39c78-eab2-fb54-c553-da8d9f26d06b
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
 - IDirect3DDevice9.SetIndices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetIndices


## -description


Sets index data.


## -parameters




### -param pIndexData [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb205865(v=VS.85).aspx">IDirect3DIndexBuffer9</a> interface, representing the index data to be set. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



When an application no longer holds a references to this interface, the interface will automatically be freed.

The <b>IDirect3DDevice9::SetIndices</b> method sets the current index array to an index buffer. The single set of indices is used to index all streams. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174369(v=VS.85).aspx">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174370(v=VS.85).aspx">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174371(v=VS.85).aspx">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174372(v=VS.85).aspx">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174391(v=VS.85).aspx">IDirect3DDevice9::GetIndices</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174595(v=VS.85).aspx">Index Buffers (Direct3D 9)</a>
 

 

