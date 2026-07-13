---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordSummary
title: DdqGetDiagnosticRecordSummary
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordSummary
description: Fetches general statistics about the diagnostic data records, filterable by producer.
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
 - DdqGetDiagnosticRecordSummary
f1_keywords:
 - DdqGetDiagnosticRecordSummary
 - diagnosticdataquery/DdqGetDiagnosticRecordSummary
---

## -description

Fetches general statistics about the diagnostic data records, filterable by producer.

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

### -param generalStats

Type: **[DIAGNOSTIC_DATA_GENERAL_STATS\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_general_stats)**
This output parameter is a pointer to the resource that contains information about the general statistics for the diagnostic data records.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

