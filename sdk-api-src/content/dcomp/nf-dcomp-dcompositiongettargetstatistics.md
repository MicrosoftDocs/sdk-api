---
UID: NF:dcomp.DCompositionGetTargetStatistics
tech.root: directcomp
title: DCompositionGetTargetStatistics
ms.date: 06/24/2021
targetos: Windows
description: 
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
api_type:
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - DCompositionGetTargetStatistics
f1_keywords:
 - DCompositionGetTargetStatistics
 - dcomp/DCompositionGetTargetStatistics
dev_langs:
 - c++
---

## -description

Gets per-target information for the specified composition frame and render target.

## -parameters

### -param frameId

Type: **COMPOSITION_FRAME_ID**

The identifier of the composition frame about which to get information.

### -param targetId

Type: **[COMPOSITION_TARGET_ID](../dcomptypes/ns-dcomptypes-composition_target_id.md)\***

The identifier of the render target about which to get information.

### -param targetStats

Type: **[COMPOSITION_TARGET_STATS](../dcomptypes/ns-dcomptypes-composition_target_stats.md)\***

Information about the specified composition frame and render target.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

[DCompositionGetStatistics](nf-dcomp-dcompositiongetstatistics.md), [DCompositionGetFrameId](nf-dcomp-dcompositiongetframeid.md), [DCompositionBoostCompositorClock](nf-dcomp-dcompositionboostcompositorclock.md), [DCompositionWaitForCompositorClock](nf-dcomp-dcompositionwaitforcompositorclock.md)
