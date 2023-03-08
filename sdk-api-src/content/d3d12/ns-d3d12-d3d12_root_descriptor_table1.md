---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR_TABLE1
title: D3D12_ROOT_DESCRIPTOR_TABLE1 (d3d12.h)
description: Describes the root signature 1.1 layout of a descriptor table as a collection of descriptor ranges that are all relative to a single base descriptor handle.
helpviewer_keywords: ["D3D12_ROOT_DESCRIPTOR_TABLE1","D3D12_ROOT_DESCRIPTOR_TABLE1 structure","d3d12/D3D12_ROOT_DESCRIPTOR_TABLE1","direct3d12.d3d12_root_descriptor_table1"]
old-location: direct3d12\d3d12_root_descriptor_table1.htm
tech.root: direct3d12
ms.assetid: 1D9D1846-2BE2-4B88-8D23-5A27173918DD
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR_TABLE1, D3D12_ROOT_DESCRIPTOR_TABLE1 structure, d3d12/D3D12_ROOT_DESCRIPTOR_TABLE1, direct3d12.d3d12_root_descriptor_table1
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
targetos: Windows
req.typenames: D3D12_ROOT_DESCRIPTOR_TABLE1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_DESCRIPTOR_TABLE1
 - d3d12/D3D12_ROOT_DESCRIPTOR_TABLE1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR_TABLE1
---

## -description

Describes the root signature 1.1 layout of a descriptor table as a collection of descriptor ranges that are all relative to a single base descriptor handle.

## -struct-fields

### -field NumDescriptorRanges

The number of descriptor ranges in the table layout.

### -field pDescriptorRanges

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1">D3D12_DESCRIPTOR_RANGE1</a> structures that describe the descriptor ranges.

## -remarks

Samplers are not allowed in the same descriptor table as constant-buffer views (CBVs), unordered-access views (UAVs), and shader-resource views (SRVs).
      

<b>D3D12_ROOT_DESCRIPTOR_TABLE1</b> is the data type of the
       <b>DescriptorTable</b> member of
        <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1">D3D12_ROOT_PARAMETER1</a>.
        Use a
        <b>D3D12_ROOT_DESCRIPTOR_TABLE1</b> when you set <b>D3D12_ROOT_PARAMETER1</b>'s <b>SlotType</b> member to <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE</a>.
      

Refer to the helper structure <a href="/windows/desktop/direct3d12/cd3dx12-root-descriptor-table1">CD3DX12_ROOT_DESCRIPTOR_TABLE1</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table">D3D12_ROOT_DESCRIPTOR_TABLE</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>