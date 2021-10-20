---
UID: NS:dcomptypes.tagCOMPOSITION_FRAME_STATS
tech.root: directcomp
title: COMPOSITION_FRAME_STATS
ms.date: 06/24/2021
targetos: Windows
description: Describes timing and composition statistics for a compositor frame.
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
req.typenames: COMPOSITION_FRAME_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - tagCOMPOSITION_FRAME_STATS
 - COMPOSITION_FRAME_STATS
f1_keywords:
 - tagCOMPOSITION_FRAME_STATS
 - dcomptypes/tagCOMPOSITION_FRAME_STATS
 - COMPOSITION_FRAME_STATS
 - dcomptypes/COMPOSITION_FRAME_STATS
dev_langs:
 - c++
---

## -description

Describes timing and composition statistics for a compositor frame.

## -struct-fields

### -field startTime

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The time the frame started.

### -field targetTime

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The frame's target time.

### -field framePeriod

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

The amount of time the frame took.

## -remarks

## -see-also

