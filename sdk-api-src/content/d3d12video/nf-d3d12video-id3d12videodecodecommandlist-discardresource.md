---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.DiscardResource
title: ID3D12VideoDecodeCommandList::DiscardResource
description: Indicate that the current contents of a resource can be discarded.
helpviewer_keywords: ["ID3D12VideoDecodeCommandList::DiscardResource","DiscardResource","ID3D12VideoDecodeCommandList.DiscardResource","ID3D12VideoDecodeCommandList::DiscardResource","ID3D12VideoDecodeCommandList.DiscardResource"]
tech.root: mf
ms.assetid: f00a49e1-d189-462f-acb7-f233239b2cf4
ms.date: 05/28/2019
f1_keywords:
- ID3D12VideoDecodeCommandList::DiscardResource
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12VideoDecodeCommandList::DiscardResource
targetos: Windows
---

# ID3D12VideoDecodeCommandList::DiscardResource


## -description

Indicate that the current contents of a resource can be discarded.  The current contents of the resource are no longer valid allowing optimizations for subsequent operations such as [ResourceBarrier](nf-d3d12video-id3d12videodecodecommandlist-discardresource.md).

## -parameters

### -param pResource

A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> interface for the resource to discard.

### -param pRegion

A pointer to a <a href="https://msdn.microsoft.com/8F0916CB-3389-40BC-8028-BA8CF9BC566B">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.

## -remarks

## -see-also
