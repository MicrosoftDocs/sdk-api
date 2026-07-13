---
UID: NS:d3d12.D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
title: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY (d3d12.h)
description: Details the adapter's support for prioritization of different command queue types.
helpviewer_keywords: ["D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY","D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure","d3d12/D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY","direct3d12.d3d12_feature_data_command_queue_priority"]
old-location: direct3d12\d3d12_feature_data_command_queue_priority.htm
tech.root: direct3d12
ms.assetid: 70DB58DB-7EE0-4E5C-8B24-22DA9347A80F
ms.date: 08/10/2022
ms.keywords: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY, D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure, d3d12/D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY, direct3d12.d3d12_feature_data_command_queue_priority
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
 - d3d12/D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
---

# D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure


## -description

Details the adapter's support for prioritization of different command queue types.

## -struct-fields

### -field CommandListType

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_In_</code>

The type of the command list you're interested in.

### -field Priority

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_In_</code>

The priority level you're interested in.

### -field PriorityForTypeIsSupported

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_Out_</code>

On return, contains true if the specfied command list type supports the specified priority level; otherwise, false.

## -remarks

Use this structure with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a> to determine the priority levels supported by various command queue types.

See the enumeration constant <b>D3D12_FEATURE_COMMAND_QUEUE_PRIORITY</b> in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>