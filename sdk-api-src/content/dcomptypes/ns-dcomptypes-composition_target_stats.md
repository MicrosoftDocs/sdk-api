---
UID: NS:dcomptypes.tagCOMPOSITION_TARGET_STATS
tech.root: directcomp
title: COMPOSITION_TARGET_STATS
ms.date: 06/24/2021
targetos: Windows
description: Contains per-target information for a composition frame and render target.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dcomptypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: COMPOSITION_TARGET_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - tagCOMPOSITION_TARGET_STATS
 - COMPOSITION_TARGET_STATS
f1_keywords:
 - tagCOMPOSITION_TARGET_STATS
 - dcomptypes/tagCOMPOSITION_TARGET_STATS
 - COMPOSITION_TARGET_STATS
 - dcomptypes/COMPOSITION_TARGET_STATS
dev_langs:
 - c++
---

## -description

Contains per-target information for a composition frame and render target.

## -struct-fields

### -field outstandingPresents

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

### -field presentTime

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

### -field vblankDuration

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

### -field presentedStats

Type: **[COMPOSITION_STATS](ns-dcomptypes-composition_stats.md)**

### -field completedStats

Type: **[COMPOSITION_STATS](ns-dcomptypes-composition_stats.md)**

## -remarks

## -see-also

[DCompositionGetStatistics](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics), [DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md)
