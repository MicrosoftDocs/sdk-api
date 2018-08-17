---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR_TABLE
title: D3D12_ROOT_DESCRIPTOR_TABLE
author: windows-sdk-content
description: Describes the root signature 1.0 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
old-location: direct3d12\d3d12_root_descriptor_table.htm
old-project: direct3d12
ms.assetid: 5A0A04AB-2053-40E0-9CD5-E344BFE9001E
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR_TABLE, D3D12_ROOT_DESCRIPTOR_TABLE structure, d3d12/D3D12_ROOT_DESCRIPTOR_TABLE, direct3d12.d3d12_descriptor_table_layout, direct3d12.d3d12_root_descriptor_table
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
req.include-header: 
req.redist: 
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
req.typenames: D3D12_ROOT_DESCRIPTOR_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_ROOT_DESCRIPTOR_TABLE structure


## -description


Describes the root signature 1.0 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
        


## -struct-fields




### -field NumDescriptorRanges

The number of descriptor ranges in the table layout.
          


### -field pDescriptorRanges

An array of <a href="https://msdn.microsoft.com/en-us/library/Dn859380(v=VS.85).aspx">D3D12_DESCRIPTOR_RANGE</a> structures that describe the descriptor ranges.
          


## -remarks



Samplers are not allowed in the same descriptor table as constant-buffer views (CBVs), unordered-access views (UAVs), and shader-resource views (SRVs).
      

<b>D3D12_ROOT_DESCRIPTOR_TABLE</b>is the data type of the
        <b>DescriptorTable</b>member of
        <a href="https://msdn.microsoft.com/en-us/library/Dn879477(v=VS.85).aspx">D3D12_ROOT_PARAMETER</a>.
        Use a
        <b>D3D12_ROOT_DESCRIPTOR_TABLE</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> member to <a href="https://msdn.microsoft.com/en-us/library/Dn879478(v=VS.85).aspx">D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186580(v=VS.85).aspx">CD3DX12_ROOT_DESCRIPTOR_TABLE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709122(v=VS.85).aspx">D3D12_ROOT_DESCRIPTOR_TABLE1</a>
 

 

