---
UID: NE:d3d12.D3D12_BACKGROUND_PROCESSING_MODE
title: D3D12_BACKGROUND_PROCESSING_MODE
description: Defines constants that specify a level of dynamic optimization to apply to GPU work that's subsequently submitted.
helpviewer_keywords: ["D3D12_BACKGROUND_PROCESSING_MODE","D3D12_BACKGROUND_PROCESSING_MODE enumeration","direct3d12.d3d12_background_processing_mode"]
tech.root: direct3d12
ms.date: 10/14/2019
ms.keywords: D3D12_BACKGROUND_PROCESSING_MODE, D3D12_BACKGROUND_PROCESSING_MODE enumeration, direct3d12.d3d12_background_processing_mode
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D3D12_BACKGROUND_PROCESSING_MODE
req.redist: 
f1_keywords:
 - D3D12_BACKGROUND_PROCESSING_MODE
 - d3d12/D3D12_BACKGROUND_PROCESSING_MODE
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
 - D3D12_BACKGROUND_PROCESSING_MODE
---

## -description

Defines constants that specify a level of dynamic optimization to apply to GPU work that's subsequently submitted.

## -enum-fields

### -field D3D12_BACKGROUND_PROCESSING_MODE_ALLOWED:0

The default setting. Specifies that the driver may instrument workloads, and dynamically recompile shaders, in a low overhead, non-intrusive manner that avoids glitching the foreground workload.

### -field D3D12_BACKGROUND_PROCESSING_MODE_ALLOW_INTRUSIVE_MEASUREMENTS

Specifies that the driver may instrument as aggressively as possible. The understanding is that causing glitches is fine while in this mode, because the current work is being submitted specifically to train the system.

### -field D3D12_BACKGROUND_PROCESSING_MODE_DISABLE_BACKGROUND_WORK

Specifies that background work should stop. This ensures that background shader recompilation won't consume CPU cycles. Available only in <b>Developer mode</b>.

### -field D3D12_BACKGROUND_PROCESSING_MODE_DISABLE_PROFILING_BY_SYSTEM

Specifies that all dynamic optimization should be disabled. For example, if you're doing an A/B performance comparison, then using this constant ensures that the driver doesn't change anything that might interfere with your results. Available only in <b>Developer mode</b>.

## -remarks

## -see-also

[Core enumerations](/windows/win32/direct3d12/direct3d-12-enumerations)

