---
UID: NE:d3d12.D3D12_META_COMMAND_PARAMETER_TYPE
title: D3D12_META_COMMAND_PARAMETER_TYPE (d3d12.h)
description: Defines constants that specify the data type of a parameter to a meta command.
helpviewer_keywords: ["D3D12_META_COMMAND_PARAMETER_TYPE","D3D12_META_COMMAND_PARAMETER_TYPE enumeration","D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV","D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT","D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV","D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS","D3D12_META_COMMAND_PARAMETER_TYPE_UINT64","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS","d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_UINT64","direct3d12.d3d12_meta_command_parameter_type"]
old-location: direct3d12\d3d12_meta_command_parameter_type.htm
tech.root: direct3d12
ms.assetid: DE2930E4-2AB1-4A32-924A-FD8754D43286
ms.date: 12/05/2018
ms.keywords: D3D12_META_COMMAND_PARAMETER_TYPE, D3D12_META_COMMAND_PARAMETER_TYPE enumeration, D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT, D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS, D3D12_META_COMMAND_PARAMETER_TYPE_UINT64, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_UINT64, direct3d12.d3d12_meta_command_parameter_type
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
req.typenames: D3D12_META_COMMAND_PARAMETER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_META_COMMAND_PARAMETER_TYPE
 - d3d12/D3D12_META_COMMAND_PARAMETER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_META_COMMAND_PARAMETER_TYPE
---

# D3D12_META_COMMAND_PARAMETER_TYPE enumeration


## -description

Defines constants that specify the data type of a parameter to a meta command.

## -enum-fields

### -field D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT:0

Specifies that the parameter is of type <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a>.

### -field D3D12_META_COMMAND_PARAMETER_TYPE_UINT64:1

Specifies that the parameter is of type <a href="/windows/desktop/WinProg/windows-data-types">UINT64</a>.

### -field D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS:2

Specifies that the parameter is a GPU virtual address.

### -field D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV:3

Specifies that the parameter is a CPU descriptor handle to a heap containing either constant buffer views, shader resource views, or unordered access views.

### -field D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV:4

Specifies that the parameter is a GPU descriptor handle to a heap containing either constant buffer views, shader resource views, or unordered access views.
