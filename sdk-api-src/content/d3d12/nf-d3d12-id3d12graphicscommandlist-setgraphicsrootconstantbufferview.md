---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView
title: ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView
author: windows-sdk-content
description: Sets a CPU descriptor handle for the constant buffer in the graphics root signature.
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootconstantbufferview.htm
old-project: direct3d12
ms.assetid: 59F6E33A-9BD8-4ED3-8CA7-235E2A0C2686
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootConstantBufferView method, ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView, ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView, SetGraphicsRootConstantBufferView, SetGraphicsRootConstantBufferView method, SetGraphicsRootConstantBufferView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView, direct3d12.id3d12graphicscommandlist_setgraphicsrootconstantbufferview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView


## -description


Sets a CPU descriptor handle for the constant buffer in the graphics root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The slot number for binding.
          


### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

The GPU virtual address of the constant buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

