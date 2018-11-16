---
UID: NS:d3d12.D3D12_DESCRIPTOR_HEAP_DESC
title: D3D12_DESCRIPTOR_HEAP_DESC
author: windows-sdk-content
description: Describes the descriptor heap.
old-location: direct3d12\d3d12_descriptor_heap_desc.htm
tech.root: direct3d12
ms.assetid: 060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_DESC, D3D12_DESCRIPTOR_HEAP_DESC structure, d3d12/D3D12_DESCRIPTOR_HEAP_DESC, direct3d12.d3d12_descriptor_heap_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - D3D12_DESCRIPTOR_HEAP_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_HEAP_DESC
req.redist: 
---

# D3D12_DESCRIPTOR_HEAP_DESC structure


## -description


Describes the descriptor heap.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/E74C78BC-B0FC-473A-B4F3-434F50A55E9F">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the types of descriptors in the heap.
          


### -field NumDescriptors

The number of descriptors in the heap.
          


### -field Flags

A combination of <a href="https://msdn.microsoft.com/727178D9-D26C-48AF-86B0-E2E171940A11">D3D12_DESCRIPTOR_HEAP_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for the heap.
          


### -field NodeMask

For single-adapter operation, set this to zero.
            If there are multiple adapter nodes, set a bit to identify the node (one of the device's physical adapters) to which the descriptor heap applies.
            Each bit in the mask corresponds to a single node.
            Only one bit must be set.
            See <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.
          


## -remarks



This structure is used by the following:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/DDDDA9AB-841A-41A4-806C-82A596AFDB61">ID3D12DescriptorHeap::GetDesc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/69EE75CB-7B3D-403D-9798-279A47754ADC">ID3D12Device::CreateDescriptorHeap</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/58677023-692C-4BA4-90B7-D568F3DD3F73">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

