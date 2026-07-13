---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordTagDistribution
title: DdqGetDiagnosticRecordTagDistribution
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordTagDistribution
description: Fetches Diagnostic Data Events per privacy tag event distribution statistics based on the specified producer names.
ms.localizationpriority: low
tech.root: security
targetos: Windows
ms.service: windows
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
 - DdqGetDiagnosticRecordTagDistribution
f1_keywords:
 - DdqGetDiagnosticRecordTagDistribution
 - diagnosticdataquery/DdqGetDiagnosticRecordTagDistribution
---

## -description

Fetches Diagnostic Data Events per privacy tag event distribution statistics based on the specified producer names.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param producerNames

Type: **[PCWSTR\*](/windows/desktop/winprog/windows-data-types)**
List of producer names to search for. A diagnostic data record that matches at least one of the producer names is included as a result in this search criteria. Use `nullptr` for this value to indicate no filter by producers.

### -param producerNameCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of producer names in the list of producer names to search for. Use `0` for this value to indicate no filter by producers.

### -param tagStats

Type: **[DIAGNOSTIC_DATA_TAG_STATS\*\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_tag_stats)**
This output parameter is a pointer to a list of DIAGNOSTIC_DATA_TAG_STATS items. Each item is a resource that contains information about a privacy tag and the number of events that have that tag.

### -param statCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of items in the DIAGNOSTIC_DATA_TAG_STATS list.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See our [**privacy statement**](/windows/privacy/windows-diagnostic-data) for information about diagnostic data privacy tags.
For more details about the tag description data type, see our [**DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION**](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_tag_description).

## -see-also

