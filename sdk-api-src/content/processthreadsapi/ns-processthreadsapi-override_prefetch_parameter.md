---
UID: NS:processthreadsapi.OVERRIDE_PREFETCH_PARAMETER
title: OVERRIDE_PREFETCH_PARAMETER
description: 
helpviewer_keywords:
 - OVERRIDE_PREFETCH_PARAMETER
tech.root: processthreadsapi
ms.date: 01/21/2024
ms.keywords: '*LPOVERRIDE_PREFETCH_PARAMETER, *POVERRIDE_PREFETCH_PARAMETER, LPOVERRIDE_PREFETCH_PARAMETER, LPOVERRIDE_PREFETCH_PARAMETER structure pointer, OVERRIDE_PREFETCH_PARAMETER, OVERRIDE_PREFETCH_PARAMETER structure, _win32_override_prefetch_parameter_str, base.override_prefetch_parameter_str, processthreadsapi/LPOVERRIDE_PREFETCH_PARAMETER, processthreadsapi/OVERRIDE_PREFETCH_PARAMETER, winbase/LPOVERRIDE_PREFETCH_PARAMETER, winbase/OVERRIDE_PREFETCH_PARAMETER'
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.typenames: OVERRIDE_PREFETCH_PARAMETER
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - OVERRIDE_PREFETCH_PARAMETER
f1_keywords:
 - OVERRIDE_PREFETCH_PARAMETER
 - processthreadsapi/OVERRIDE_PREFETCH_PARAMETER
dev_langs:
 - c++
---

# OVERRIDE_PREFETCH_PARAMETER structure

## -description

Provides additional control over App Launch Prefetch (ALPF) functionality.

## -struct-fields

### -field Value

A unique identifier for differentiating an application view or mode.

## -remarks

App Launch Prefetch (ALPF) brings data and code pages into memory from disk before it's demanded. Prefetching monitors the data and code accessed during application startups and uses that information at the beginning of subsequent startups to read the code and data proactively in an efficient manner to improve performance.

If ALPF predicts incorrectly, the wrong pages may be fetched, slowing app launches. Applications with different "Views", such as Outlook Mail View or  Calendar View, may cause this issue by needing different pages of memory depending on the View. To solve this, applications can pass a Prefetch Parameter to their launch through the command line, which will provide a unique identifier to differentiate between Views or other scenarios that cause ALPF’s standard prediction to fail.

## -see-also
