---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.SetPredication
title: ID3D12VideoEncodeCommandList::SetPredication
ms.date: 11/4/2019
targetos: Windows
description: Specifies that subsequent commands should not be performed if the predicate value passes the specified operation. (ID3D12VideoEncodeCommandList::SetPredication)
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
 - ID3D12VideoEncodeCommandList::SetPredication
f1_keywords:
 - ID3D12VideoEncodeCommandList::SetPredication
 - d3d12video/ID3D12VideoEncodeCommandList::SetPredication
dev_langs:
 - c++
---

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
