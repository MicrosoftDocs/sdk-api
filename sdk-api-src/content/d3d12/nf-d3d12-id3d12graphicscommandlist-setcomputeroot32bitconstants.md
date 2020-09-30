---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRoot32BitConstants
title: ID3D12GraphicsCommandList::SetComputeRoot32BitConstants (d3d12.h)
description: Sets a group of constants in the compute root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetComputeRoot32BitConstants method","ID3D12GraphicsCommandList.SetComputeRoot32BitConstants","ID3D12GraphicsCommandList::SetComputeRoot32BitConstants","SetComputeRoot32BitConstants","SetComputeRoot32BitConstants method","SetComputeRoot32BitConstants method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetComputeRoot32BitConstants","direct3d12.id3d12graphicscommandlist_setcomputeroot32bitconstants"]
old-location: direct3d12\id3d12graphicscommandlist_setcomputeroot32bitconstants.htm
tech.root: direct3d12
ms.assetid: A4623522-4748-4999-80EC-E6AC8934136A
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRoot32BitConstants method, ID3D12GraphicsCommandList.SetComputeRoot32BitConstants, ID3D12GraphicsCommandList::SetComputeRoot32BitConstants, SetComputeRoot32BitConstants, SetComputeRoot32BitConstants method, SetComputeRoot32BitConstants method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRoot32BitConstants, direct3d12.id3d12graphicscommandlist_setcomputeroot32bitconstants
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::SetComputeRoot32BitConstants
 - d3d12/ID3D12GraphicsCommandList::SetComputeRoot32BitConstants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetComputeRoot32BitConstants
---

# ID3D12GraphicsCommandList::SetComputeRoot32BitConstants


## -description

Sets a group of constants in the compute root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.

### -param Num32BitValuesToSet [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of constants to set in the root signature.

### -param pSrcData [in]

Type: <b>const void*</b>

The source data for the group of constants to set.

### -param DestOffsetIn32BitValues [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset, in 32-bit values, to set the first constant of the group in the root signature.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>