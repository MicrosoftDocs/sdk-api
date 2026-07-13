---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordLocaleTagAtIndex
title: DdqGetDiagnosticRecordLocaleTagAtIndex
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordLocaleTagAtIndex
description: Fetches tag description at the specified index in the resource pointed to by the HDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION handle.
ms.localizationpriority: low
tech.root: security
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: DiagnosticDataQuery.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - diagnosticdataquery.h
api_name:
 - DdqGetDiagnosticRecordLocaleTagAtIndex
f1_keywords:
 - DdqGetDiagnosticRecordLocaleTagAtIndex
 - diagnosticdataquery/DdqGetDiagnosticRecordLocaleTagAtIndex
---

## -description

Fetches tag description at the specified index in the resource pointed to by the HDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION resource.

## -parameters

### -param hTagDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the list of tag descriptions.

### -param index

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The index of the tag description to be fetched.

### -param tagDescription

Type: **[DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION\*](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_tag_description.md)**
This outpoint parameter is a pointer to the tag description that was fetched.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also
