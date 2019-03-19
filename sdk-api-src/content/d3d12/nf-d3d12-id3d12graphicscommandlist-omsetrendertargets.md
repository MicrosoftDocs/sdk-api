---
UID: NF:d3d12.ID3D12GraphicsCommandList.OMSetRenderTargets
title: ID3D12GraphicsCommandList::OMSetRenderTargets (d3d12.h)
author: windows-sdk-content
description: Sets CPU descriptor handles for the render targets and depth stencil.
old-location: direct3d12\id3d12graphicscommandlist_omsetrendertargets.htm
tech.root: direct3d12
ms.assetid: FE565AA2-FA34-4824-870E-9C4C7C19C93C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12GraphicsCommandList interface,OMSetRenderTargets method, ID3D12GraphicsCommandList.OMSetRenderTargets, ID3D12GraphicsCommandList::OMSetRenderTargets, OMSetRenderTargets, OMSetRenderTargets method, OMSetRenderTargets method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::OMSetRenderTargets, direct3d12.id3d12graphicscommandlist_omsetrendertargets
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
 - ID3D12GraphicsCommandList.OMSetRenderTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::OMSetRenderTargets


## -description


Sets CPU descriptor handles for the render targets and depth stencil.
        


## -parameters




### -param NumRenderTargetDescriptors [in]

Type: <b>UINT</b>

The number of entries in the <i>pRenderTargetDescriptors</i> array.
          


### -param pRenderTargetDescriptors [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

Specifies an array of <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a> structures that describe the CPU descriptor handles that represents the start of the heap of render target descriptors.
          


### -param RTsSingleHandleToDescriptorRange [in]

Type: <b>BOOL</b>

<b>True</b> means the handle passed in is the pointer to a contiguous range of <i>NumRenderTargetDescriptors</i>  descriptors.  This case is useful if the set of descriptors to bind already happens to be contiguous in memory (so all that’s needed is a handle to the first one).  For example, if  <i>NumRenderTargetDescriptors</i> is 3 then the memory layout is taken as follows:

<img alt="Memory layout with parameter set to true" src="./images/oms_true.png"/>
In this case the driver dereferences the handle and then increments the memory being pointed to.

<b>False</b> means that the handle is the first of an array of <i>NumRenderTargetDescriptors</i> handles.  The false case allows an application to bind a set of descriptors from different locations at once. Again assuming that <i>NumRenderTargetDescriptors</i> is 3, the memory layout is taken as follows:

<img alt="Memory layout with parameter set to false" src="./images/oms_false.png"/>
In this case the driver dereferences three handles that are expected to be adjacent to each other in memory.


### -param pDepthStencilDescriptor [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a> structure that describes the CPU descriptor handle that represents the start of the heap that holds the depth stencil descriptor.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

