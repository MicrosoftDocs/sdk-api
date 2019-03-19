---
UID: NS:d3d12.D3D12_META_COMMAND_DESC
title: D3D12_META_COMMAND_DESC (d3d12.h)
author: windows-sdk-content
description: Describes a meta command.
old-location: direct3d12\d3d12_meta_command_desc.htm
tech.root: direct3d12
ms.assetid: 0783068A-21D0-4316-9F50-8566535747C8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_META_COMMAND_DESC, D3D12_META_COMMAND_DESC structure, d3d12/D3D12_META_COMMAND_DESC, direct3d12.d3d12_meta_command_desc
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
 - D3D12_META_COMMAND_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_META_COMMAND_DESC
req.redist: 
---

# D3D12_META_COMMAND_DESC structure


## -description


Describes a meta command.


## -struct-fields




### -field Id

Type: <b><a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a></b>

A <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> uniquely identifying the meta command.


### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The meta command name.


### -field InitializationDirtyState

Type: <b><a href="https://msdn.microsoft.com/261585A3-CDF1-4559-9E14-9EE710F1D8D9">D3D12_GRAPHICS_STATES</a></b>

Declares the command list states that are modified by the call to initialize the meta command. If all state bits are set, then that's equivalent to calling <a href="https://msdn.microsoft.com/F7C230CE-0E28-466A-8A54-601ECEC6CDC9">ID3D12GraphicsCommandList::ClearState</a>.


### -field ExecutionDirtyState

Type: <b><a href="https://msdn.microsoft.com/261585A3-CDF1-4559-9E14-9EE710F1D8D9">D3D12_GRAPHICS_STATES</a></b>

Declares the command list states that are modified by the call to execute the meta command. If all state bits are set, then that's equivalent to calling <a href="https://msdn.microsoft.com/F7C230CE-0E28-466A-8A54-601ECEC6CDC9">ID3D12GraphicsCommandList::ClearState</a>.

