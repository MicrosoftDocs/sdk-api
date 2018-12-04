---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootUnorderedAccessView
title: ID3D12GraphicsCommandList::SetGraphicsRootUnorderedAccessView
author: windows-sdk-content
description: Sets a CPU descriptor handle for the unordered-access-view resource in the graphics root signature.
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootunorderedaccessview.htm
tech.root: direct3d12
ms.assetid: 7EF90634-0A33-42F5-880D-8E22910FAB47
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootUnorderedAccessView method, ID3D12GraphicsCommandList.SetGraphicsRootUnorderedAccessView, ID3D12GraphicsCommandList::SetGraphicsRootUnorderedAccessView, SetGraphicsRootUnorderedAccessView, SetGraphicsRootUnorderedAccessView method, SetGraphicsRootUnorderedAccessView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootUnorderedAccessView, direct3d12.id3d12graphicscommandlist_setgraphicsrootunorderedaccessview
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12GraphicsCommandList.SetGraphicsRootUnorderedAccessView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::SetGraphicsRootUnorderedAccessView


## -description


Sets a CPU descriptor handle for the unordered-access-view resource in the graphics root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The slot number for binding.
          


### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

The GPU virtual address of the buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

