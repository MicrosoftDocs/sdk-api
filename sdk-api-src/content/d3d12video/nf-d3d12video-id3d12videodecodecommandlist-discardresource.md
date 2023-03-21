---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.DiscardResource
title: ID3D12VideoDecodeCommandList::DiscardResource
description: Indicate that the current contents of a resource can be discarded. (ID3D12VideoDecodeCommandList::DiscardResource)
helpviewer_keywords: ["ID3D12VideoDecodeCommandList::DiscardResource","DiscardResource","ID3D12VideoDecodeCommandList.DiscardResource","ID3D12VideoDecodeCommandList::DiscardResource","ID3D12VideoDecodeCommandList.DiscardResource"]
tech.root: mf
ms.assetid: f00a49e1-d189-462f-acb7-f233239b2cf4
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDecodeCommandList::DiscardResource, DiscardResource, ID3D12VideoDecodeCommandList.DiscardResource, ID3D12VideoDecodeCommandList::DiscardResource, ID3D12VideoDecodeCommandList.DiscardResource
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
 - ID3D12VideoDecodeCommandList::DiscardResource
 - d3d12video/ID3D12VideoDecodeCommandList::DiscardResource
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::DiscardResource
---

# ID3D12VideoDecodeCommandList::DiscardResource


## -description

Indicate that the current contents of a resource can be discarded.  The current contents of the resource are no longer valid allowing optimizations for subsequent operations such as [ResourceBarrier](nf-d3d12video-id3d12videodecodecommandlist-discardresource.md).

## -parameters

### -param pResource

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface for the resource to discard.

### -param pRegion

A pointer to a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.

## -remarks

## -see-also
