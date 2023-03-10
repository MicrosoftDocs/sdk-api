---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.WriteBufferImmediate
title: ID3D12VideoDecodeCommandList::WriteBufferImmediate
description: Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream. (ID3D12VideoDecodeCommandList::WriteBufferImmediate)
helpviewer_keywords: ["ID3D12VideoDecodeCommandList::WriteBufferImmediate","WriteBufferImmediate","ID3D12VideoDecodeCommandList.WriteBufferImmediate","ID3D12VideoDecodeCommandList::WriteBufferImmediate","ID3D12VideoDecodeCommandList.WriteBufferImmediate"]
tech.root: mf
ms.assetid: cdc54874-4d54-4595-8f19-17dc35ff670c
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDecodeCommandList::WriteBufferImmediate, WriteBufferImmediate, ID3D12VideoDecodeCommandList.WriteBufferImmediate, ID3D12VideoDecodeCommandList::WriteBufferImmediate, ID3D12VideoDecodeCommandList.WriteBufferImmediate
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
 - ID3D12VideoDecodeCommandList::WriteBufferImmediate
 - d3d12video/ID3D12VideoDecodeCommandList::WriteBufferImmediate
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::WriteBufferImmediate
---

# ID3D12VideoDecodeCommandList::WriteBufferImmediate


## -description

Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.

## -parameters

### -param Count

The number of elements in the *pParams* and *pModes* arrays.

### -param pParams

The address of an array of [D3D12_WRITEBUFFERIMMEDIATE_PARAMETER](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter) structures of size *Count*.

### -param pModes

The address of an array of [D3D12_WRITEBUFFERIMMEDIATE_MODE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode) structures of size *Count*. The default value is <b>null</b>. Passing <b>null</b> causes the system to write all immediate values using **D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT**.

## -remarks

The capability for this feature is specified with [D3D12_FEATURE_DATA_D3D12_OPTIONS3::WriteBufferImmediateSupportFlags](../d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3.md)

## -see-also
