---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_GENERAL_STATS
title: DIAGNOSTIC_DATA_GENERAL_STATS
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_GENERAL_STATS, DIAGNOSTIC_DATA_GENERAL_STATS
description: This resource contains general statistics about a set of diagnostic data records.
tech.root: security
targetos: Windows
ms.service: windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquerytypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: DIAGNOSTIC_DATA_GENERAL_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_GENERAL_STATS
 - DIAGNOSTIC_DATA_GENERAL_STATS
f1_keywords:
 - tagDIAGNOSTIC_DATA_GENERAL_STATS
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_GENERAL_STATS
 - DIAGNOSTIC_DATA_GENERAL_STATS
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_GENERAL_STATS
---

## -description

This resource contains general statistics about a set of diagnostic data records.

## -struct-fields

### -field optInLevel

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
This identifies the device's current diagnostic data opt-in level (Security = 0, Basic = 1, Enhanced = 2, and Full = 3). See remarks for more details.

### -field transcriptSizeBytes

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**
The collective size in bytes for the diagnostic data records.

### -field oldestEventTimestamp

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**
The timestamp of the oldest event among the diagnostic data records.

### -field totalEventCountLast24Hours

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Total number of events among the diagnostic data records within the last 24 hours.

### -field averageDailyEvents

Type: **[FLOAT](/windows/desktop/winprog/windows-data-types)**
The average number of events sent per day in this set of diagnostic data records.

## -remarks

See our [**privacy statement**](/windows/privacy/windows-diagnostic-data) for information about diagnostic data opt-in levels.

## -see-also

