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

# D3D12_ROOT_DESCRIPTOR_TABLE1 structure


## -description



          Describes the root signature 1.1 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
        


## -struct-fields




### -field NumDescriptorRanges


            The number of descriptor ranges in the table layout.
          


### -field pDescriptorRanges


            An array of <a href="https://msdn.microsoft.com/EFC36053-6FD1-4D2E-8214-66B50F0CC0D5">D3D12_DESCRIPTOR_RANGE1</a> structures that describe the descriptor ranges.
          


## -remarks




        Samplers are not allowed in the same descriptor table as constant-buffer views (CBVs), unordered-access views (UAVs), and shader-resource views (SRVs).
      

<b>D3D12_ROOT_DESCRIPTOR_TABLE1</b>
        is the data type of the
        <b>DescriptorTable</b>
        member of
        <a href="https://msdn.microsoft.com/615B8ABF-FD80-4254-976B-9E587CE9F12E">D3D12_ROOT_PARAMETER1</a>.
        Use a
        <b>D3D12_ROOT_DESCRIPTOR_TABLE1</b> when you set <b>D3D12_ROOT_PARAMETER1</b>'s <b>SlotType</b> member to <a href="d3d12_root_parameter_type.htm">D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE</a>.
      

Refer to the helper structure <a href="https://msdn.microsoft.com/82AC1948-92AA-4A4D-B443-717E9BF3046D">CD3DX12_ROOT_DESCRIPTOR_TABLE1</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/5A0A04AB-2053-40E0-9CD5-E344BFE9001E">D3D12_ROOT_DESCRIPTOR_TABLE</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

