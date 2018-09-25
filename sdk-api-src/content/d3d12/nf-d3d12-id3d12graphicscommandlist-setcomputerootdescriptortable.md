---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootDescriptorTable
title: ID3D12GraphicsCommandList::SetComputeRootDescriptorTable
author: windows-sdk-content
description: Sets a descriptor table into the compute root signature.
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootdescriptortable.htm
tech.root: direct3d12
ms.assetid: DC05D64A-39D0-4EF2-A9FE-956B499386F2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootDescriptorTable method, ID3D12GraphicsCommandList.SetComputeRootDescriptorTable, ID3D12GraphicsCommandList::SetComputeRootDescriptorTable, SetComputeRootDescriptorTable, SetComputeRootDescriptorTable method, SetComputeRootDescriptorTable method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootDescriptorTable, direct3d12.id3d12graphicscommandlist_setcomputerootdescriptortable
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
 - ID3D12GraphicsCommandList.SetComputeRootDescriptorTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::SetComputeRootDescriptorTable


## -description


Sets a descriptor table into the compute root signature.


## -parameters




### -param RootParameterIndex [in]

Type: <b>UINT</b>

The slot number for binding.
          


### -param BaseDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/16D09788-D527-4D9F-A6EF-648F42A426B5">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A GPU_descriptor_handle object for the base descriptor to set.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

