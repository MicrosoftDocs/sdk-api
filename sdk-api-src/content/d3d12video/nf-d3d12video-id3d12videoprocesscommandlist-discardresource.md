---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.DiscardResource
title: ID3D12VideoProcessCommandList::DiscardResource
description: Indicates that the current contents of a resource can be discarded.
helpviewer_keywords: ["ID3D12VideoProcessCommandList::DiscardResource","DiscardResource","ID3D12VideoProcessCommandList.DiscardResource","ID3D12VideoProcessCommandList::DiscardResource","ID3D12VideoProcessCommandList.DiscardResource"]
tech.root: mf
ms.assetid: ee2e1ce5-e6ab-4e49-9177-2ff98dca420e
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::DiscardResource, DiscardResource, ID3D12VideoProcessCommandList.DiscardResource, ID3D12VideoProcessCommandList::DiscardResource, ID3D12VideoProcessCommandList.DiscardResource
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - ID3D12VideoProcessCommandList::DiscardResource
 - d3d12video/ID3D12VideoProcessCommandList::DiscardResource
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::DiscardResource
---

# ID3D12VideoProcessCommandList::DiscardResource


## -description

Indicates that the current contents of a resource can be discarded.  The current contents of the resource are no longer valid allowing optimizations for subsequent operations such as [ResourceBarrier](nf-d3d12video-id3d12videoprocesscommandlist-discardresource.md).

## -parameters

### -param pResource

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface for the resource to discard.

### -param pRegion

A pointer to a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.

## -remarks

## -see-also