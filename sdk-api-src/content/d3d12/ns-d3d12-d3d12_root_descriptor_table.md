---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_ROOT_DESCRIPTOR_TABLE structure


## -description



          Describes the root signature 1.0 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
        


## -struct-fields




### -field NumDescriptorRanges


            The number of descriptor ranges in the table layout.
          


### -field pDescriptorRanges


            An array of <a href="https://msdn.microsoft.com/6F1C4D05-3E08-4353-B5B9-4C4270FC1403">D3D12_DESCRIPTOR_RANGE</a> structures that describe the descriptor ranges.
          


## -remarks




        Samplers are not allowed in the same descriptor table as constant-buffer views (CBVs), unordered-access views (UAVs), and shader-resource views (SRVs).
      

<b>D3D12_ROOT_DESCRIPTOR_TABLE</b>
        is the data type of the
        <b>DescriptorTable</b>
        member of
        <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a>.
        Use a
        <b>D3D12_ROOT_DESCRIPTOR_TABLE</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> member to <a href="d3d12_root_parameter_type.htm">D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/154B4C50-4E94-471C-A44E-F120A84F007C">CD3DX12_ROOT_DESCRIPTOR_TABLE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/1D9D1846-2BE2-4B88-8D23-5A27173918DD">D3D12_ROOT_DESCRIPTOR_TABLE1</a>
 

 

