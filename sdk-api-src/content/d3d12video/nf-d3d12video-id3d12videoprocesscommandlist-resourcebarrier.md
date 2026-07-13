---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.ResourceBarrier
title: ID3D12VideoProcessCommandList::ResourceBarrier
description: Notifies the driver that it needs to synchronize multiple accesses to resources. (ID3D12VideoProcessCommandList::ResourceBarrier)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::ResourceBarrier","ResourceBarrier","ID3D12VideoProcessCommandList.ResourceBarrier","ID3D12VideoProcessCommandList::ResourceBarrier","ID3D12VideoProcessCommandList.ResourceBarrier"]
tech.root: mf
ms.assetid: 9c37e5aa-b9f7-4e72-ae08-cf0403d0bc5a
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::ResourceBarrier, ResourceBarrier, ID3D12VideoProcessCommandList.ResourceBarrier, ID3D12VideoProcessCommandList::ResourceBarrier, ID3D12VideoProcessCommandList.ResourceBarrier
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
 - ID3D12VideoProcessCommandList::ResourceBarrier
 - d3d12video/ID3D12VideoProcessCommandList::ResourceBarrier
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::ResourceBarrier
---

# ID3D12VideoProcessCommandList::ResourceBarrier


## -description

Notifies the driver that it needs to synchronize multiple accesses to resources.

## -parameters

### -param NumBarriers

Type: <b>UINT</b>

The number of submitted barrier descriptions.

### -param pBarriers

Type: <b>const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a>*</b>

Pointer to an array of barrier descriptions.

## -remarks

## -see-also
