---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.WriteBufferImmediate
title: ID3D12VideoEncodeCommandList::WriteBufferImmediate
ms.date: 11/4/2019
targetos: Windows
description: Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream. (ID3D12VideoEncodeCommandList::WriteBufferImmediate)
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
 - ID3D12VideoEncodeCommandList::WriteBufferImmediate
f1_keywords:
 - ID3D12VideoEncodeCommandList::WriteBufferImmediate
 - d3d12video/ID3D12VideoEncodeCommandList::WriteBufferImmediate
dev_langs:
 - c++
---

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
