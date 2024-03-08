---
UID: NF:dcomp.DCompositionWaitForCompositorClock
tech.root: directcomp
title: DCompositionWaitForCompositorClock
ms.date: 06/24/2021
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
req.lib: 
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

## -remarks

## -see-also

[DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md), [DCompositionGetStatistics](nf-dcomp-dcompositiongetstatistics.md), [DCompositionGetFrameId](nf-dcomp-dcompositiongetframeid.md), [DCompositionBoostCompositorClock](nf-dcomp-dcompositionboostcompositorclock.md)
