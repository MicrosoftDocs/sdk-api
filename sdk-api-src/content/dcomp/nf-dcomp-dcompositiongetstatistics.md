---
UID: NF:dcomp.DCompositionGetStatistics
tech.root: directcomp
title: DCompositionGetStatistics
ms.date: 06/24/2021
targetos: Windows
description: Gets basic information about the composition frame and a list of render target ID's that are part of the frame.
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
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - DCompositionGetStatistics
f1_keywords:
 - DCompositionGetStatistics
 - dcomp/DCompositionGetStatistics
dev_langs:
 - c++
---

## -description

Gets basic information about the composition frame and a list of render target ID's that are part of the frame.

## -parameters

### -param frameId

Type: **COMPOSITION_FRAME_ID**

The identifier of the composition frame about which to get information.

### -param frameStats

Type: **[COMPOSITION_FRAME_STATS](../dcomptypes/ns-dcomptypes-composition_frame_stats.md)\***

A struct that contains information about the composition frame.

### -param targetIdCount

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The number of render targets about which to get information.

### -param targetIds

Type: **[COMPOSITION_TARGET_ID](../dcomptypes/ns-dcomptypes-composition_target_id.md)\***

The identifiers of the render targets about which to get information.

### -param actualTargetIdCount

Type: **[UINT](/windows/win32/WinProg/windows-data-types)\***

The actual number of render targets.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

[DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md), [DCompositionGetFrameId](nf-dcomp-dcompositiongetframeid.md), [DCompositionBoostCompositorClock](nf-dcomp-dcompositionboostcompositorclock.md), [DCompositionWaitForCompositorClock](nf-dcomp-dcompositionwaitforcompositorclock.md)
