---
UID: NS:dcomptypes.tagCOMPOSITION_STATS
tech.root: directcomp
title: COMPOSITION_STATS
ms.date: 06/24/2021
targetos: Windows
description: Describes timing and composition information.
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
req.typenames: COMPOSITION_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - tagCOMPOSITION_STATS
 - COMPOSITION_STATS
f1_keywords:
 - tagCOMPOSITION_STATS
 - dcomptypes/tagCOMPOSITION_STATS
 - COMPOSITION_STATS
 - dcomptypes/COMPOSITION_STATS
dev_langs:
 - c++
---

## -description

Describes timing and composition information.

## -struct-fields

### -field presentCount

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The running total count of times that a frame was presented to the target.

### -field refreshCount

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The running total count of v-blanks at which the last frame was presented to the target.

### -field virtualRefreshCount

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

### -field time

Type: **[UINT64](/windows/win32/WinProg/windows-data-types)**

## -remarks

## -see-also

