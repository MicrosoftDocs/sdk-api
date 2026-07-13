---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordStats
title: DdqGetDiagnosticRecordStats
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordStats
description: Fetches the filtered event transcript Diagnostic Data record stats. The filtering on statistics returned is performed using the input parameter, DIAGNOSTIC_DATA_SEARCH_CRITERIA filter. The record state describes how many records matching the search criteria are available, and returns parameters used for further querying of data. One of the uses of this API is to check if there have been changes since the last time data was queried for. A change in the output parameters indicate a change in state of the event transcript record state.
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
 - DdqGetDiagnosticRecordStats
f1_keywords:
 - DdqGetDiagnosticRecordStats
 - diagnosticdataquery/DdqGetDiagnosticRecordStats
---

## -description

Fetches the filtered event transcript Diagnostic Data record stats. The filtering on statistics returned is performed using the input parameter, DIAGNOSTIC_DATA_SEARCH_CRITERIA filter. The record state describes how many records matching the search criteria are available, and returns parameters used for further querying of data. One of the uses of this API is to check if there have been changes since the last time data was queried for. A change in the output parameters indicate a change in state of the event transcript record state.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param searchCriteria

Type: **[DIAGNOSTIC_DATA_SEARCH_CRITERIA\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_search_criteria)**
Pointer to the resource that contains the search criteria for this operation. This resource contains criteria such as producers, categories, and tags.

### -param recordCount

Type: **[UINT32\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is the pointer to the number of records that match on the search criteria.

### -param minRowId

Type: **[INT64\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is the pointer to the minimum row id of the record that matches on the search criteria.

### -param maxRowId

Type: **[INT64\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is the pointer to the maximum row id of the record that matches on the search criteria.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

