---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_RECORD
title: DIAGNOSTIC_DATA_RECORD
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_RECORD, DIAGNOSTIC_DATA_RECORD
description: This resource describes an individual diagnostic data record (event).
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
req.typenames: DIAGNOSTIC_DATA_RECORD
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_RECORD
 - DIAGNOSTIC_DATA_RECORD
f1_keywords:
 - tagDIAGNOSTIC_DATA_RECORD
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_RECORD
 - DIAGNOSTIC_DATA_RECORD
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_RECORD
---

## -description

This resource describes an individual diagnostic data record (event).

## -struct-fields

### -field rowId

Type: **[INT64](/windows/desktop/com/structure-of-com-error-codes)**
The row ID of the record.

### -field timestamp

Type: **[UINT64](/windows/desktop/com/structure-of-com-error-codes)**
The timestamp for when the record was processed.

### -field eventKeywords

Type: **[UINT64](/windows/desktop/com/structure-of-com-error-codes)**
The keywords associated with this event.

### -field fullEventName

Type: **[LPWSTR](/windows/desktop/com/structure-of-com-error-codes)**
The full event name.

### -field providerGroupGuid

Type: **[LPWSTR](/windows/desktop/com/structure-of-com-error-codes)**
The provider group GUID for this event.

### -field producerName

Type: **[LPWSTR](/windows/desktop/com/structure-of-com-error-codes)**
The name of the producer associated with this event.

### -field privacyTags

Type: **[INT32\*](/windows/desktop/com/structure-of-com-error-codes)**
A list of privacy tag IDs for this event.

### -field privacyTagCount

Type: **[UINT32](/windows/desktop/com/structure-of-com-error-codes)**
The number of privacy tags associated with this event.

### -field categoryIds

Type: **[INT32\*](/windows/desktop/com/structure-of-com-error-codes)**
A list of the categories associated with this event.

### -field categoryIdCount

Type: **[UINT32](/windows/desktop/com/structure-of-com-error-codes)**
The number of categories associated with this event.

### -field isCoreData

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**
`TRUE` if this record is core data. `FALSE` otherwise.

### -field extra1

### -field extra2

### -field extra3

## -remarks

- For more information about events and providers, see [**Event Tracing**](/windows/win32/etw/event-tracing-portal). 
- For information about how a producer is defined, see [**DIAGNOSTIC_DATA_EVENT_PRODUCER_DESCRIPTION**](./ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description.md).
- For information about how a tag is defined, see [**DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION**](./ns-diagnosticdataquerytypes-diagnostic_data_event_tag_description.md).
- For information about how a category is defined, see [**DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION**](./ns-diagnosticdataquerytypes-diagnostic_data_event_category_description.md).
- For more details on what is core data, see our [**privacy statement**](/windows/privacy/windows-diagnostic-data).

## -see-also