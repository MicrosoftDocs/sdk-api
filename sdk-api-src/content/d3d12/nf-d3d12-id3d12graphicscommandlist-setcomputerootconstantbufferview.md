---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootConstantBufferView
title: ID3D12GraphicsCommandList::SetComputeRootConstantBufferView (d3d12.h)
author: windows-sdk-content
description: Sets a CPU descriptor handle for the constant buffer in the compute root signature.
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootconstantbufferview.htm
tech.root: direct3d12
ms.assetid: AEAB392F-365F-4EDB-AC57-FFAC40C800C0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootConstantBufferView method, ID3D12GraphicsCommandList.SetComputeRootConstantBufferView, ID3D12GraphicsCommandList::SetComputeRootConstantBufferView, SetComputeRootConstantBufferView, SetComputeRootConstantBufferView method, SetComputeRootConstantBufferView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootConstantBufferView, direct3d12.id3d12graphicscommandlist_setcomputerootconstantbufferview
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetComputeRootConstantBufferView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::SetComputeRootConstantBufferView


## -description


Sets a CPU descriptor handle for the constant buffer in the compute root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b>UINT</b>

The slot number for binding.
          


### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

Specifies the D3D12_GPU_VIRTUAL_ADDRESS of the constant buffer.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

