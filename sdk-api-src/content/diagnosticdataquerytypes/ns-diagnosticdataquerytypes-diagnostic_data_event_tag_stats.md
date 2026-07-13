---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_EVENT_TAG_STATS
title: DIAGNOSTIC_DATA_EVENT_TAG_STATS
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_EVENT_TAG_STATS, DIAGNOSTIC_DATA_EVENT_TAG_STATS
description: A resource that includes a privacy tag and how many events have this privacy tag.
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
req.typenames: DIAGNOSTIC_DATA_EVENT_TAG_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_EVENT_TAG_STATS
 - DIAGNOSTIC_DATA_EVENT_TAG_STATS
f1_keywords:
 - tagDIAGNOSTIC_DATA_EVENT_TAG_STATS
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_EVENT_TAG_STATS
 - DIAGNOSTIC_DATA_EVENT_TAG_STATS
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_EVENT_TAG_STATS
---

## -description

A resource that includes a privacy tag and how many events have this privacy tag.

## -struct-fields

### -field privacyTag

Type: **[INT32](/windows/desktop/winprog/windows-data-types)**
The numeric identifier for this privacy tag.

### -field eventCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of events that have this privacy tag.

## -remarks

See our [**privacy statement**](/windows/privacy/windows-diagnostic-data) for information about diagnostic data privacy tags.

## -see-also

