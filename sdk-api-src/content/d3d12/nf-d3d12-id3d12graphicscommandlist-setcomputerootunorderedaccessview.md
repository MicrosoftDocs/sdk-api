---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView
title: ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView
author: windows-sdk-content
description: Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootunorderedaccessview.htm
old-project: direct3d12
ms.assetid: 7C91B305-ABB2-4355-AA4B-3E1641ACF9E0
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootUnorderedAccessView method, ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView, ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView, SetComputeRootUnorderedAccessView, SetComputeRootUnorderedAccessView method, SetComputeRootUnorderedAccessView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView, direct3d12.id3d12graphicscommandlist_setcomputerootunorderedaccessview
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
 - ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView


## -description



          Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.
        


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
 

 

