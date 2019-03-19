---
UID: NE:d3d12.D3D12_DESCRIPTOR_HEAP_TYPE
title: D3D12_DESCRIPTOR_HEAP_TYPE (d3d12.h)
author: windows-sdk-content
description: Specifies a type of descriptor heap.
old-location: direct3d12\d3d12_descriptor_heap_type.htm
tech.root: direct3d12
ms.assetid: E74C78BC-B0FC-473A-B4F3-434F50A55E9F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_TYPE, D3D12_DESCRIPTOR_HEAP_TYPE enumeration, D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV, D3D12_DESCRIPTOR_HEAP_TYPE_DSV, D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES, D3D12_DESCRIPTOR_HEAP_TYPE_RTV, D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_DSV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_RTV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER, direct3d12.d3d12_descriptor_heap_type
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DESCRIPTOR_HEAP_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_HEAP_TYPE
req.redist: 
---

# D3D12_DESCRIPTOR_HEAP_TYPE enumeration


## -description


Specifies a type of descriptor heap.
        


## -enum-fields




### -field D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV

The descriptor heap for the combination of constant-buffer, shader-resource, and unordered-access views.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER

The descriptor heap for the sampler.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_RTV

The descriptor heap for the render-target view.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_DSV

The descriptor heap for the depth-stencil view.
          


### -field D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES

The number of types of descriptor heaps.
          


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED">D3D12_DESCRIPTOR_HEAP_DESC</a> structure, and the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/F995EF34-74FF-4FCA-A018-E2F48DF92450">CopyDescriptors</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6DA1FCDA-042C-4727-9814-B8F57E14CD51">CopyDescriptorsSimple</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4593C153-913A-49DF-ADDC-6FB1E19D3D17">GetDescriptorHandleIncrementSize</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/58677023-692C-4BA4-90B7-D568F3DD3F73">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

