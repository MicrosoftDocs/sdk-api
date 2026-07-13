---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_EVENT_BINARY_STATS
title: DIAGNOSTIC_DATA_EVENT_BINARY_STATS
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_EVENT_BINARY_STATS, DIAGNOSTIC_DATA_EVENT_BINARY_STATS
description: A resource that describes this binary and the amount of diagnostic data it has sent.
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
req.typenames: DIAGNOSTIC_DATA_EVENT_BINARY_STATS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_EVENT_BINARY_STATS
 - DIAGNOSTIC_DATA_EVENT_BINARY_STATS
f1_keywords:
 - tagDIAGNOSTIC_DATA_EVENT_BINARY_STATS
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_EVENT_BINARY_STATS
 - DIAGNOSTIC_DATA_EVENT_BINARY_STATS
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_EVENT_BINARY_STATS
---

## -description

A resource that describes this binary and the amount of diagnostic data it has sent.

## -struct-fields

### -field moduleName

Type: **[LPWSTR](/windows/desktop/winprog/windows-data-types)**
The full name of the module or binary.

### -field friendlyModuleName

Type: **[LPWSTR](/windows/desktop/winprog/windows-data-types)**
The friendly name of the module or binary.

### -field eventCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of events sent by this module or binary.

### -field uploadSizeBytes

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**
The number of bytes sent by this module or binary.

## -remarks

## -see-also

