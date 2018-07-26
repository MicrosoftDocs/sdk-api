---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable
title: ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable
author: windows-sdk-content
description: Sets a descriptor table into the graphics root signature.
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootdescriptortable.htm
old-project: direct3d12
ms.assetid: AF182E9D-6A85-42B2-ADE4-490756AEDCE7
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootDescriptorTable method, ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable, ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable, SetGraphicsRootDescriptorTable, SetGraphicsRootDescriptorTable method, SetGraphicsRootDescriptorTable method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable, direct3d12.id3d12graphicscommandlist_setgraphicsrootdescriptortable
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
 - ID3D12GraphicsCommandList.SetGraphicsRootDescriptorTable
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable


## -description


Sets a descriptor table into the graphics root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The slot number for binding.
          


### -param BaseDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/16D09788-D527-4D9F-A6EF-648F42A426B5">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A GPU_descriptor_handle object for the base descriptor to set.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

