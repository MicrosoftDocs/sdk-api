---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.DiscardResource
title: ID3D12VideoEncodeCommandList::DiscardResource
ms.date: 11/4/2019
targetos: Windows
description: Indicate that the current contents of a resource can be discarded. (ID3D12VideoEncodeCommandList::DiscardResource)
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoEncodeCommandList::DiscardResource
f1_keywords:
 - ID3D12VideoEncodeCommandList::DiscardResource
 - d3d12video/ID3D12VideoEncodeCommandList::DiscardResource
dev_langs:
 - c++
---

## -description

Indicate that the current contents of a resource can be discarded.  The current contents of the resource are no longer valid allowing optimizations for subsequent operations such as [ResourceBarrier](nf-d3d12video-id3d12videodecodecommandlist-discardresource.md).

## -parameters

### -param pResource

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface for the resource to discard.

### -param pRegion

A pointer to a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.

## -remarks

## -see-also
