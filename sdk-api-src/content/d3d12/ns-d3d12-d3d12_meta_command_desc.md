---
UID: NS:d3d12.D3D12_META_COMMAND_DESC
title: D3D12_META_COMMAND_DESC (d3d12.h)
description: Describes a meta command.
helpviewer_keywords: ["D3D12_META_COMMAND_DESC","D3D12_META_COMMAND_DESC structure","d3d12/D3D12_META_COMMAND_DESC","direct3d12.d3d12_meta_command_desc"]
old-location: direct3d12\d3d12_meta_command_desc.htm
tech.root: direct3d12
ms.assetid: 0783068A-21D0-4316-9F50-8566535747C8
ms.date: 12/05/2018
ms.keywords: D3D12_META_COMMAND_DESC, D3D12_META_COMMAND_DESC structure, d3d12/D3D12_META_COMMAND_DESC, direct3d12.d3d12_meta_command_desc
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
req.typenames: D3D12_META_COMMAND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_META_COMMAND_DESC
 - d3d12/D3D12_META_COMMAND_DESC
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
 - D3D12_META_COMMAND_DESC
---

# D3D12_META_COMMAND_DESC structure


## -description

Describes a meta command.

## -struct-fields

### -field Id

Type: <b><a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a></b>

A <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> uniquely identifying the meta command.

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The meta command name.

### -field InitializationDirtyState

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_graphics_states">D3D12_GRAPHICS_STATES</a></b>

Declares the command list states that are modified by the call to initialize the meta command. If all state bits are set, then that's equivalent to calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate">ID3D12GraphicsCommandList::ClearState</a>.

### -field ExecutionDirtyState

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_graphics_states">D3D12_GRAPHICS_STATES</a></b>

Declares the command list states that are modified by the call to execute the meta command. If all state bits are set, then that's equivalent to calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate">ID3D12GraphicsCommandList::ClearState</a>.