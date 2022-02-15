---
UID: NE:d3d12.D3D12_PIPELINE_STATE_FLAGS
title: D3D12_PIPELINE_STATE_FLAGS (d3d12.h)
description: Flags to control pipeline state.
helpviewer_keywords: ["D3D12_PIPELINE_STATE_FLAGS","D3D12_PIPELINE_STATE_FLAGS enumeration","D3D12_PIPELINE_STATE_FLAG_NONE","D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG","d3d12/D3D12_PIPELINE_STATE_FLAGS","d3d12/D3D12_PIPELINE_STATE_FLAG_NONE","d3d12/D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG","direct3d12.d3d12_pipeline_state_flags"]
old-location: direct3d12\d3d12_pipeline_state_flags.htm
tech.root: direct3d12
ms.assetid: DAE5C06B-ED1F-4B35-812E-31E26B51704C
ms.date: 12/05/2018
ms.keywords: D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_FLAGS enumeration, D3D12_PIPELINE_STATE_FLAG_NONE, D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG, d3d12/D3D12_PIPELINE_STATE_FLAGS, d3d12/D3D12_PIPELINE_STATE_FLAG_NONE, d3d12/D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG, direct3d12.d3d12_pipeline_state_flags
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
req.typenames: D3D12_PIPELINE_STATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_PIPELINE_STATE_FLAGS
 - d3d12/D3D12_PIPELINE_STATE_FLAGS
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
 - D3D12_PIPELINE_STATE_FLAGS
---

# D3D12_PIPELINE_STATE_FLAGS enumeration


## -description

Flags to control pipeline state.

## -enum-fields

### -field D3D12_PIPELINE_STATE_FLAG_NONE:0

Indicates no flags.

### -field D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG:0x1

Indicates that the pipeline state should be compiled with additional information to assist debugging.
          This can only be set on WARP devices.

## -remarks

This enum is used by the <b>Flags</b> member of the
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structures.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
