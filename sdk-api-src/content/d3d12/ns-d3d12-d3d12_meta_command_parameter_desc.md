---
UID: NS:d3d12.D3D12_META_COMMAND_PARAMETER_DESC
title: D3D12_META_COMMAND_PARAMETER_DESC (d3d12.h)
description: Describes a parameter to a meta command.
helpviewer_keywords: ["D3D12_META_COMMAND_PARAMETER_DESC","D3D12_META_COMMAND_PARAMETER_DESC structure","d3d12/D3D12_META_COMMAND_PARAMETER_DESC","direct3d12.d3d12_meta_command_parameter_desc"]
old-location: direct3d12\d3d12_meta_command_parameter_desc.htm
tech.root: direct3d12
ms.assetid: F4314919-B7E1-4628-867D-462F8F9A48FA
ms.date: 12/05/2018
ms.keywords: D3D12_META_COMMAND_PARAMETER_DESC, D3D12_META_COMMAND_PARAMETER_DESC structure, d3d12/D3D12_META_COMMAND_PARAMETER_DESC, direct3d12.d3d12_meta_command_parameter_desc
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
req.typenames: D3D12_META_COMMAND_PARAMETER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_META_COMMAND_PARAMETER_DESC
 - d3d12/D3D12_META_COMMAND_PARAMETER_DESC
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
 - D3D12_META_COMMAND_PARAMETER_DESC
---

# D3D12_META_COMMAND_PARAMETER_DESC structure


## -description

Describes a parameter to a meta command.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The parameter name.

### -field Type

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type">D3D12_META_COMMAND_PARAMETER_TYPE</a></b>

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type">D3D12_META_COMMAND_PARAMETER_TYPE</a> specifying the parameter type.

### -field Flags

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags">D3D12_META_COMMAND_PARAMETER_FLAGS</a></b>

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags">D3D12_META_COMMAND_PARAMETER_FLAGS</a> specifying the parameter flags.

### -field RequiredResourceState

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a></b>

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> specifying the expected state of a resource parameter.

### -field StructureOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The 4-byte aligned offset for this parameter, within the structure containing the parameter values, which you pass when creating/initializing/executing the meta command, as appropriate.