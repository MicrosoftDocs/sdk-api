---
UID: NE:d3d12.D3D12_MEASUREMENTS_ACTION
title: D3D12_MEASUREMENTS_ACTION
description: Defines constants that specify what should be done with the results of earlier workload instrumentation.
helpviewer_keywords: ["D3D12_MEASUREMENTS_ACTION","D3D12_MEASUREMENTS_ACTION enumeration","direct3d12.d3d12_measurements_action"]
tech.root: direct3d12
ms.date: 10/14/2019
ms.keywords: D3D12_MEASUREMENTS_ACTION, D3D12_MEASUREMENTS_ACTION enumeration, direct3d12.d3d12_measurements_action
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
req.typenames: D3D12_MEASUREMENTS_ACTION
req.redist: 
f1_keywords:
 - D3D12_MEASUREMENTS_ACTION
 - d3d12/D3D12_MEASUREMENTS_ACTION
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
 - D3D12_MEASUREMENTS_ACTION
---

## -description

Defines constants that specify what should be done with the results of earlier workload instrumentation.

## -enum-fields

### -field D3D12_MEASUREMENTS_ACTION_KEEP_ALL:0

The default setting. Specifies that all results should be kept.

### -field D3D12_MEASUREMENTS_ACTION_COMMIT_RESULTS

Specifies that the driver has seen all the data that it's ever going to, so it should stop waiting for more and go ahead compiling optimized shaders.

### -field D3D12_MEASUREMENTS_ACTION_COMMIT_RESULTS_HIGH_PRIORITY

Like <b>D3D12_MEASUREMENTS_ACTION_COMMIT_RESULTS</b>, but also specifies that your application doesn't care about glitches, so the runtime should ignore the usual idle priority rules and go ahead using as many threads as possible to get shader recompiles done fast. Available only in <b>Developer mode</b>.

### -field D3D12_MEASUREMENTS_ACTION_DISCARD_PREVIOUS

Specifies that the optimization state should be reset; hinting that whatever has previously been measured no longer applies.

## -remarks

## -see-also

[Core enumerations](/windows/win32/direct3d12/direct3d-12-enumerations)

