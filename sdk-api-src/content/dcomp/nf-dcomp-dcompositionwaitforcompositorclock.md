---
UID: NF:dcomp.DCompositionWaitForCompositorClock
tech.root: directcomp
title: DCompositionWaitForCompositorClock
ms.date: 10/31/2025
targetos: Windows
description: Halts a thread until the next signal from the compositor clock occurs.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dcomp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dcomp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomp.h
api_name:
 - DCompositionWaitForCompositorClock
f1_keywords:
 - DCompositionWaitForCompositorClock
 - dcomp/DCompositionWaitForCompositorClock
dev_langs:
 - c++
---

## -description

Halts a thread until the next signal from the compositor clock occurs.

## -parameters

### -param count

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The number of _`handles`_.

### -param handles

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)\***

Handles to events for which the compositor clock should send signals.

### -param timeoutInMs

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

Amount of time in milliseconds to wait before the operation times out.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

Returns a status code (an **NTSTATUS** value) that indicates the success or failure of the function. If the method succeeds, then it will return `STATUS_SUCCESS`. If the display is off, then the function returns immediately with **STATUS_GRAPHICS_PRESENT_OCCLUDED**. For other **NTSTATUS** values, see [NTSTATUS values](/openspecs/windows_protocols/ms-erref/596a1078-e883-4972-9bbc-49e60bebca55).

## -remarks

## -see-also

[DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md), [DCompositionGetStatistics](nf-dcomp-dcompositiongetstatistics.md), [DCompositionGetFrameId](nf-dcomp-dcompositiongetframeid.md), [DCompositionBoostCompositorClock](nf-dcomp-dcompositionboostcompositorclock.md)
