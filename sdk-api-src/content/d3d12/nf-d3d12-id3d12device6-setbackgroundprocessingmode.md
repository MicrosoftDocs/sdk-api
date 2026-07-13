---
UID: NF:d3d12.ID3D12Device6.SetBackgroundProcessingMode
title: ID3D12Device6::SetBackgroundProcessingMode
description: Sets the mode for driver background processing optimizations.
helpviewer_keywords: ["ID3D12Device6 interface","SetBackgroundProcessingMode method","ID3D12Device6.SetBackgroundProcessingMode","ID3D12Device6::SetBackgroundProcessingMode","SetBackgroundProcessingMode","SetBackgroundProcessingMode method","SetBackgroundProcessingMode method","ID3D12Device6 interface","direct3d12.id3d12device6_setbackgroundprocessingmode","d3d12/ID3D12Device6::SetBackgroundProcessingMode"]
tech.root: direct3d12
ms.date: 10/14/2019
ms.keywords: ID3D12Device6 interface,SetBackgroundProcessingMode method, ID3D12Device6.SetBackgroundProcessingMode, ID3D12Device6::SetBackgroundProcessingMode, SetBackgroundProcessingMode, SetBackgroundProcessingMode method, SetBackgroundProcessingMode method,ID3D12Device6 interface, direct3d12.id3d12device6_setbackgroundprocessingmode, d3d12/ID3D12Device6::SetBackgroundProcessingMode
req.construct-type: function
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
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12Device6::SetBackgroundProcessingMode
 - d3d12/ID3D12Device6::SetBackgroundProcessingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device6::SetBackgroundProcessingMode
---

## -description

Sets the mode for driver background processing optimizations.

## -parameters

### -param Mode [in]

Type: **[D3D12_BACKGROUND_PROCESSING_MODE](./ne-d3d12-d3d12_background_processing_mode.md)**

The level of dynamic optimization to apply to GPU work that's subsequently submitted.

### -param MeasurementsAction [in]

Type: **[D3D12_MEASUREMENTS_ACTION](./ne-d3d12-d3d12_measurements_action.md)**

The action to take with the results of earlier workload instrumentation.

### -param hEventToSignalUponCompletion [in]

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

An optional handle to signal when the function is complete. For example, if *MeasurementsAction* is set to [D3D12_MEASUREMENTS_ACTION_COMMIT_RESULTS](./ne-d3d12-d3d12_measurements_action.md), then *hEventToSignalUponCompletion* is signaled when all resulting compilations have finished.

### -param pbFurtherMeasurementsDesired [out]

Type: **[BOOL](/windows/win32/winprog/windows-data-types)\***

An optional pointer to a Boolean value. The function sets the value to `true` to indicate that you should continue profiling, otherwise, `false`.

## -returns

## -remarks

A graphics driver can use idle-priority background CPU threads to dynamically recompile shader programs. That can improve GPU performance by specializing shader code to better match details of the hardware that it's running on, and/or the context in which it's being used.

As a developer, you don't have to do anything to benefit from this feature (over time, as drivers adopt background processing optimizations, existing shaders will automatically be tuned more efficiently). But, when you're profiling your code, you'll probably want to call **SetBackgroundProcessingMode** to make sure that any driver background processing optimizations have taken place before you take timing measurements. Here's an example.

```cpp
SetBackgroundProcessingMode(
    D3D12_BACKGROUND_PROCESSING_MODE_ALLOW_INTRUSIVE_MEASUREMENTS,
    D3D_MEASUREMENTS_ACTION_KEEP_ALL,
    nullptr, nullptr);
 
// Here, prime the system by rendering some typical content.
// For example, a level flythrough.
 
SetBackgroundProcessingMode(
    D3D12_BACKGROUND_PROCESSING_MODE_ALLOWED,
    D3D12_MEASUREMENTS_ACTION_COMMIT_RESULTS,
    nullptr, nullptr);
 
// Here, continue rendering. This time with dynamic optimizations applied.
// And then take your measurements.
```

[PIX](https://devblogs.microsoft.com/pix/) automatically uses **SetBackgroundProcessingMode**&mdash;first to prime the system,and then to prevent any further changes from taking place in the middle of its analysis. PIX waits on an event (to make sure all background shader recompiles have finished) before it starts taking measurements.

## -see-also
