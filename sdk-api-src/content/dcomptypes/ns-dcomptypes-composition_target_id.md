---
UID: NS:dcomptypes.tagCOMPOSITION_TARGET_ID
tech.root: directcomp
title: COMPOSITION_TARGET_ID
ms.date: 06/24/2021
targetos: Windows
description: Contains information about a composition render target.
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
req.typenames: COMPOSITION_TARGET_ID
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - tagCOMPOSITION_TARGET_ID
 - COMPOSITION_TARGET_ID
f1_keywords:
 - tagCOMPOSITION_TARGET_ID
 - dcomptypes/tagCOMPOSITION_TARGET_ID
 - COMPOSITION_TARGET_ID
 - dcomptypes/COMPOSITION_TARGET_ID
dev_langs:
 - c++
---

## -description

Contains information about a composition render target.

## -struct-fields

### -field displayAdapterLuid

Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid)**

The locally unique identifier (LUID) of the display adapter to which the monitor is connected.

### -field renderAdapterLuid

Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid)**

The locally unique identifier (LUID) of the render adapter.

### -field vidPnSourceId

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The unique ID of the video present source.

### -field vidPnTargetId

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The unique ID of the video present target.

### -field uniqueId

A unique identifier for this `COMPOSITION_TARGET_ID`.

## -remarks

## -see-also

[DCompositionGetStatistics](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics), [DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md)
