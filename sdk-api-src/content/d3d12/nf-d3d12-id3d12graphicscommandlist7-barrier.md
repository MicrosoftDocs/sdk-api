---
UID: NF:d3d12.ID3D12GraphicsCommandList7.Barrier
title: ID3D12GraphicsCommandList7::Barrier
description: Adds a collection of barriers into a graphics command list recording.
helpviewer_keywords:
 - Barrier
tech.root: direct3d12
ms.date: 11/01/2022
req.construct-type: function
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
f1_keywords:
 - ID3D12GraphicsCommandList7::Barrier
 - d3d12/ID3D12GraphicsCommandList7::Barrier
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12GraphicsCommandList7::Barrier
---

## -description

Adds a collection of barriers into a graphics command list recording.

Requires the DirectX 12 Agility SDK 1.608 or later.

## -parameters

### -param NumBarrierGroups

Number of barrier groups pointed to by *pBarrierGroups*.

### -param pBarrierGroups

Pointer to an array of [D3D12_BARRIER_GROUP](/windows/win32/api/d3d12/ns-d3d12-d3d12_barrier_group) objects.

## -remarks

## -see-also
