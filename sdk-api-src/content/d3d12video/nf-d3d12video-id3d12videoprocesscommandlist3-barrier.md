---
UID: NF:d3d12video.ID3D12VideoProcessCommandList3.Barrier
title: ID3D12VideoProcessCommandList3::Barrier
description: Adds a collection of barriers into a video process command list recording.
tech.root: mf
ms.date: 11/01/2022
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoProcessCommandList3::Barrier
f1_keywords:
 - ID3D12VideoProcessCommandList3::Barrier
 - d3d12video/ID3D12VideoProcessCommandList3::Barrier
dev_langs:
 - c++
helpviewer_keywords:
 - Barrier
---

## -description

Adds a collection of barriers into a video process command list recording.

Requires the DirectX 12 Agility SDK 1.7 or later.

## -parameters

### -param NumBarrierGroups

Number of barrier groups pointed to by *pBarrierGroups*.

### -param pBarrierGroups

Pointer to an array of [D3D12_BARRIER_GROUP](/windows/win32/api/d3d12/ns-d3d12-d3d12_barrier_group) objects.

## -remarks

## -see-also
