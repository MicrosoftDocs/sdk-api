---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR_TABLE1
title: D3D12_ROOT_DESCRIPTOR_TABLE1 (d3d12.h)
author: windows-sdk-content
description: Describes the root signature 1.1 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
old-location: direct3d12\d3d12_root_descriptor_table1.htm
tech.root: direct3d12
ms.assetid: 1D9D1846-2BE2-4B88-8D23-5A27173918DD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR_TABLE1, D3D12_ROOT_DESCRIPTOR_TABLE1 structure, d3d12/D3D12_ROOT_DESCRIPTOR_TABLE1, direct3d12.d3d12_root_descriptor_table1
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
 - d3d12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR_TABLE1
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_DESCRIPTOR_TABLE1
req.redist: 
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
      

<b>D3D12_ROOT_DESCRIPTOR_TABLE1</b>is the data type of the
        <b>DescriptorTable</b>member of
        <a href="https://msdn.microsoft.com/615B8ABF-FD80-4254-976B-9E587CE9F12E">D3D12_ROOT_PARAMETER1</a>.
        Use a
        <b>D3D12_ROOT_DESCRIPTOR_TABLE1</b> when you set <b>D3D12_ROOT_PARAMETER1</b>'s <b>SlotType</b> member to <a href="https://msdn.microsoft.com/en-us/library/Dn879478(v=VS.85).aspx">D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE</a>.
      

Refer to the helper structure <a href="https://msdn.microsoft.com/82AC1948-92AA-4A4D-B443-717E9BF3046D">CD3DX12_ROOT_DESCRIPTOR_TABLE1</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/5A0A04AB-2053-40E0-9CD5-E344BFE9001E">D3D12_ROOT_DESCRIPTOR_TABLE</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

