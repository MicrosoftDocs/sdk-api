---
UID: NS:d3d12.D3D12_FEATURE_DATA_QUERY_META_COMMAND
title: D3D12_FEATURE_DATA_QUERY_META_COMMAND
description: Indicates the level of support that the adapter provides for metacommands.
helpviewer_keywords: ["D3D12_FEATURE_DATA_QUERY_META_COMMAND"]
tech.root: direct3d12
ms.date: 09/19/2019
ms.keywords: D3D12_FEATURE_DATA_QUERY_META_COMMAND
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_QUERY_META_COMMAND
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_QUERY_META_COMMAND
 - d3d12/D3D12_FEATURE_DATA_QUERY_META_COMMAND
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_QUERY_META_COMMAND
---

## -description

Indicates the level of support that the adapter provides for metacommands.

## -struct-fields

### -field CommandId

Type: <b>[GUID](../guiddef/ns-guiddef-guid.md)</b>

The fixed GUID that identifies the metacommand to query about.

### -field NodeMask

Type: <b>[UINT](/windows/win32/winprog/windows-data-types)</b>

For single GPU operation, this is zero. If there are multiple GPU nodes, a bit is set to identify a node (the device's physical adapter). Each bit in the mask corresponds to a single node. Only 1 bit must be set. Refer to [Multi-adapter systems](/windows/win32/direct3d12/multi-engine).

### -field pQueryInputData

Type: <b> const [void](/windows/win32/winprog/windows-data-types)\*</b>

A pointer to a buffer containing the query input data. Allocate *QueryInputDataSizeInBytes* bytes.

### -field QueryInputDataSizeInBytes

Type: <b>[SIZE_T](/windows/win32/winprog/windows-data-types)</b>

The size of the buffer pointed to by *pQueryInputData*, in bytes.

### -field pQueryOutputData

Type: <b>[void](/windows/win32/winprog/windows-data-types)\*</b>

A pointer to a buffer containing the query output data.

### -field QueryOutputDataSizeInBytes

Type: <b>[SIZE_T](/windows/win32/winprog/windows-data-types)</b>

The size of the buffer pointed to by *pQueryOutputData*, in bytes.

## -remarks

## -see-also
