---
UID: NS:d3d12.D3D12_META_COMMAND_PARAMETER_DESC
title: D3D12_META_COMMAND_PARAMETER_DESC (d3d12.h)
author: windows-sdk-content
description: Describes a parameter to a meta command.
old-location: direct3d12\d3d12_meta_command_parameter_desc.htm
tech.root: direct3d12
ms.assetid: F4314919-B7E1-4628-867D-462F8F9A48FA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_META_COMMAND_PARAMETER_DESC, D3D12_META_COMMAND_PARAMETER_DESC structure, d3d12/D3D12_META_COMMAND_PARAMETER_DESC, direct3d12.d3d12_meta_command_parameter_desc
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
 - D3D12_META_COMMAND_PARAMETER_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_META_COMMAND_PARAMETER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_META_COMMAND_PARAMETER_DESC structure


## -description


Describes a parameter to a meta command.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The parameter name.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/DE2930E4-2AB1-4A32-924A-FD8754D43286">D3D12_META_COMMAND_PARAMETER_TYPE</a></b>

A <a href="https://msdn.microsoft.com/DE2930E4-2AB1-4A32-924A-FD8754D43286">D3D12_META_COMMAND_PARAMETER_TYPE</a> specifying the parameter type.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/E81F4F8E-BD9B-4965-B55C-358797A40651">D3D12_META_COMMAND_PARAMETER_FLAGS</a></b>

A <a href="https://msdn.microsoft.com/E81F4F8E-BD9B-4965-B55C-358797A40651">D3D12_META_COMMAND_PARAMETER_FLAGS</a> specifying the parameter flags.


### -field RequiredResourceState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>

A <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> specifying the expected state of a resource parameter.


### -field StructureOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The 4-byte aligned offset for this parameter, within the structure containing the parameter values, which you pass when creating/initializing/executing the meta command, as appropriate.

