---
UID: NE:d3d12.D3D12_META_COMMAND_PARAMETER_TYPE
title: D3D12_META_COMMAND_PARAMETER_TYPE (d3d12.h)
author: windows-sdk-content
description: Defines constants that specify the data type of a parameter to a meta command.
old-location: direct3d12\d3d12_meta_command_parameter_type.htm
tech.root: direct3d12
ms.assetid: DE2930E4-2AB1-4A32-924A-FD8754D43286
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_META_COMMAND_PARAMETER_TYPE, D3D12_META_COMMAND_PARAMETER_TYPE enumeration, D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT, D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS, D3D12_META_COMMAND_PARAMETER_TYPE_UINT64, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS, d3d12/D3D12_META_COMMAND_PARAMETER_TYPE_UINT64, direct3d12.d3d12_meta_command_parameter_type
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
 - D3D12_META_COMMAND_PARAMETER_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_META_COMMAND_PARAMETER_TYPE
req.redist: 
---

# D3D12_META_COMMAND_PARAMETER_TYPE enumeration


## -description


Defines constants that specify the data type of a parameter to a meta command.


## -enum-fields




### -field D3D12_META_COMMAND_PARAMETER_TYPE_FLOAT

Specifies that the parameter is of type <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a>.


### -field D3D12_META_COMMAND_PARAMETER_TYPE_UINT64

Specifies that the parameter is of type <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>.


### -field D3D12_META_COMMAND_PARAMETER_TYPE_GPU_VIRTUAL_ADDRESS

Specifies that the parameter is a GPU virtual address.


### -field D3D12_META_COMMAND_PARAMETER_TYPE_CPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV

Specifies that the parameter is a CPU descriptor handle to a heap containing either constant buffer views, shader resource views, or unordered access views.


### -field D3D12_META_COMMAND_PARAMETER_TYPE_GPU_DESCRIPTOR_HANDLE_HEAP_TYPE_CBV_SRV_UAV

Specifies that the parameter is a GPU descriptor handle to a heap containing either constant buffer views, shader resource views, or unordered access views.

