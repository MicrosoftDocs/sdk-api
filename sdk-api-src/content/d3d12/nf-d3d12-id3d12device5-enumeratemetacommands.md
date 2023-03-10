---
UID: NF:d3d12.ID3D12Device5.EnumerateMetaCommands
title: ID3D12Device5::EnumerateMetaCommands (d3d12.h)
description: Queries reflection metadata about available meta commands.
helpviewer_keywords: ["EnumerateMetaCommands","EnumerateMetaCommands method","EnumerateMetaCommands method","ID3D12Device5 interface","ID3D12Device5 interface","EnumerateMetaCommands method","ID3D12Device5.EnumerateMetaCommands","ID3D12Device5::EnumerateMetaCommands","d3d12/ID3D12Device5::EnumerateMetaCommands","direct3d12.id3d12device5_enumeratemetacommands"]
old-location: direct3d12\id3d12device5_enumeratemetacommands.htm
tech.root: direct3d12
ms.assetid: 71A16704-487F-49AA-B229-61CCD15B3037
ms.date: 12/05/2018
ms.keywords: EnumerateMetaCommands, EnumerateMetaCommands method, EnumerateMetaCommands method,ID3D12Device5 interface, ID3D12Device5 interface,EnumerateMetaCommands method, ID3D12Device5.EnumerateMetaCommands, ID3D12Device5::EnumerateMetaCommands, d3d12/ID3D12Device5::EnumerateMetaCommands, direct3d12.id3d12device5_enumeratemetacommands
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device5::EnumerateMetaCommands
 - d3d12/ID3D12Device5::EnumerateMetaCommands
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.h
api_name:
 - ID3D12Device5.EnumerateMetaCommands
---

## -description

Queries reflection metadata about available meta commands.

## -parameters

### -param pNumMetaCommands

Type: [in, out] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a <a href="/windows/desktop/WinProg/windows-data-types">UINT</a> containing the number of meta commands to query for. This field determines the size of the <i>pDescs</i> array, unless <i>pDescs</i> is <b>nullptr</b>.

### -param pDescs

Type: [out, optional] **[D3D12_META_COMMAND_DESC](./ns-d3d12-d3d12_meta_command_desc.md)\***

An optional pointer to an array of [D3D12_META_COMMAND_DESC](./ns-d3d12-d3d12_meta_command_desc.md) containing the descriptions of the available meta commands. Pass `nullptr` to have the number of available meta commands returned in <i>pNumMetaCommands</i>.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12device5.md">ID3D12Device5</a>
