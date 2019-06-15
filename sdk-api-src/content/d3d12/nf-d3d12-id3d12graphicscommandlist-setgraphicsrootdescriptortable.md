---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable
title: ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable (d3d12.h)
author: windows-sdk-content
description: Sets a descriptor table into the graphics root signature.
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootdescriptortable.htm
tech.root: direct3d12
ms.assetid: AF182E9D-6A85-42B2-ADE4-490756AEDCE7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootDescriptorTable method, ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable, ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable, SetGraphicsRootDescriptorTable, SetGraphicsRootDescriptorTable method, SetGraphicsRootDescriptorTable method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable, direct3d12.id3d12graphicscommandlist_setgraphicsrootdescriptortable
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
 - ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable


## -description


Sets a descriptor table into the graphics root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.
          


### -param BaseDescriptor [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A GPU_descriptor_handle object for the base descriptor to set.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
 

 

