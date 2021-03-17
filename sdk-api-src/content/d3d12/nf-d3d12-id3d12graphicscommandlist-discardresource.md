---
UID: NF:d3d12.ID3D12GraphicsCommandList.DiscardResource
title: ID3D12GraphicsCommandList::DiscardResource (d3d12.h)
description: Discards a resource.
helpviewer_keywords: ["DiscardResource","DiscardResource method","DiscardResource method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","DiscardResource method","ID3D12GraphicsCommandList.DiscardResource","ID3D12GraphicsCommandList::DiscardResource","d3d12/ID3D12GraphicsCommandList::DiscardResource","direct3d12.id3d12graphicscommandlist_discardresource"]
old-location: direct3d12\id3d12graphicscommandlist_discardresource.htm
tech.root: direct3d12
ms.assetid: 2F4DBA5B-F586-4126-8867-BEE650F6D161
ms.date: 12/05/2018
ms.keywords: DiscardResource, DiscardResource method, DiscardResource method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,DiscardResource method, ID3D12GraphicsCommandList.DiscardResource, ID3D12GraphicsCommandList::DiscardResource, d3d12/ID3D12GraphicsCommandList::DiscardResource, direct3d12.id3d12graphicscommandlist_discardresource
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
 - ID3D12GraphicsCommandList::DiscardResource
 - d3d12/ID3D12GraphicsCommandList::DiscardResource
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
 - ID3D12GraphicsCommandList.DiscardResource
---

## -description

Indicates that the contents of a resource don't need to be preserved. The function may re-initialize resource metadata in some cases.

## -parameters

### -param pResource

Type: [in] <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface for the resource to discard.

### -param pRegion

Type: [in, optional] <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region">D3D12_DISCARD_REGION</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.

## -remarks

The semantics of <b>DiscardResource</b> change based on the command list type.

For <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE_DIRECT</a>, the following two rules apply:

<ul>
<li>When a resource has the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET</a> flag, <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_RENDER_TARGET</a> resource barrier state.</li>
<li>When a resource has the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG _ALLOW_DEPTH_STENCIL</a> flag, <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_DEPTH_WRITE</a>.
</li>
</ul>
For <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE_COMPUTE</a>, the following rule applies:

<ul>
<li>The resource must have the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS</a> flag, and <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a> resource barrier state.</li>
</ul>
<b>DiscardResource</b> is not supported on command lists with either <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE_BUNDLE</a> nor <b>D3D12_COMMAND_LIST_TYPE_COPY</b>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>

<a href="/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>