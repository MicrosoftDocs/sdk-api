---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.SetPredication
title: ID3D12VideoProcessCommandList::SetPredication
description: Specifies that subsequent commands should not be performed if the predicate value passes the specified operation. (ID3D12VideoProcessCommandList::SetPredication)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::SetPredication","SetPredication","ID3D12VideoProcessCommandList.SetPredication","ID3D12VideoProcessCommandList::SetPredication","ID3D12VideoProcessCommandList.SetPredication"]
tech.root: mf
ms.assetid: 0ac39382-e939-4f20-b99d-0b3d9eac1ddc
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::SetPredication, SetPredication, ID3D12VideoProcessCommandList.SetPredication, ID3D12VideoProcessCommandList::SetPredication, ID3D12VideoProcessCommandList.SetPredication
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
 - ID3D12VideoProcessCommandList::SetPredication
 - d3d12video/ID3D12VideoProcessCommandList::SetPredication
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::SetPredication
---

# ID3D12VideoProcessCommandList::SetPredication


## -description

Specifies that subsequent commands should not be performed if the predicate value passes the specified operation.

## -parameters

### -param pBuffer

A pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the buffer from which to read the 64-bit predication value.

### -param AlignedBufferOffset

The UINT64-aligned buffer offset.

### -param Operation

A member of the [D3D12_PREDICATION_OP](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op) enumeration specifying the predicate operation.

## -remarks

## -see-also
