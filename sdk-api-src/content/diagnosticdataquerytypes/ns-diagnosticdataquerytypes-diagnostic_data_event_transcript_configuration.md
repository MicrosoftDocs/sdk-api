---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
title: DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION, DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
description: Event transcript configuration details such as maximum storage size and hours of data history.
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
req.typenames: DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
 - DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
f1_keywords:
 - tagDIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
 - DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION
---

## -description

Event transcript configuration details such as maximum storage size and hours of data history.

## -struct-fields

### -field hoursOfHistoryToKeep

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Number of hours of event history to keep. When an event has been stored for longer than this amount of time, it will be dropped.

### -field maxStoreMegabytes

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Maximum storage size (in megabytes) of event history to keep. When event store exceeds this size, events will be removed from the store starting with the oldest event.

### -field requestedMaxStoreMegabytes

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The requested storage size (in megabytes) of event history to keep.

## -remarks

For more details on how configurations work, see [**Diagnostic Data Viewer overview**](/windows/privacy/diagnostic-data-viewer-overview)

## -see-also

