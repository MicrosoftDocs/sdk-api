---
UID: NF:d3d12.ID3D12GraphicsCommandList.SOSetTargets
title: ID3D12GraphicsCommandList::SOSetTargets (d3d12.h)
description: Sets the stream output buffer views.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SOSetTargets method","ID3D12GraphicsCommandList.SOSetTargets","ID3D12GraphicsCommandList::SOSetTargets","SOSetTargets","SOSetTargets method","SOSetTargets method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SOSetTargets","direct3d12.id3d12graphicscommandlist_sosettargets"]
old-location: direct3d12\id3d12graphicscommandlist_sosettargets.htm
tech.root: direct3d12
ms.assetid: 40683FD6-5B9F-411C-AC0A-6641E0A3D688
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SOSetTargets method, ID3D12GraphicsCommandList.SOSetTargets, ID3D12GraphicsCommandList::SOSetTargets, SOSetTargets, SOSetTargets method, SOSetTargets method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SOSetTargets, direct3d12.id3d12graphicscommandlist_sosettargets
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
 - ID3D12GraphicsCommandList::SOSetTargets
 - d3d12/ID3D12GraphicsCommandList::SOSetTargets
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
 - ID3D12GraphicsCommandList.SOSetTargets
---

# ID3D12GraphicsCommandList::SOSetTargets


## -description

Sets the stream output buffer views.

## -parameters

### -param StartSlot [in]

Type: <b>UINT</b>

Index into the device's zero-based array to begin setting stream output buffers.

### -param NumViews [in]

Type: <b>UINT</b>

The number of entries in the <i>pViews</i> array.

### -param pViews [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view">D3D12_STREAM_OUTPUT_BUFFER_VIEW</a>*</b>

Specifies an array of  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view">D3D12_STREAM_OUTPUT_BUFFER_VIEW</a> structures.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>