---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordPage
title: DdqGetDiagnosticRecordPage
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordPage
description: Fetches a page (batch) of filtered records. The filtering on records returned is performed internally using the input parameters DIAGNOSTIC_DATA_SEARCH_CRITERIA searchCriteria, pageRecordCount, offset and baseRowId.
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
 - DdqGetDiagnosticRecordPage
f1_keywords:
 - DdqGetDiagnosticRecordPage
 - diagnosticdataquery/DdqGetDiagnosticRecordPage
---

## -description

Fetches a page (batch) of filtered records. The filtering on records returned is performed internally using the input parameters DIAGNOSTIC_DATA_SEARCH_CRITERIA searchCriteria, pageRecordCount, offset and baseRowId.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param searchCriteria

Type: **[DIAGNOSTIC_DATA_SEARCH_CRITERIA\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_search_criteria)**
Pointer to the resource that contains the search criteria for this operation. This resource contains criteria such as producers, categories, and tags.

### -param offset

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Filters results by returning records with rowId that start at the offset from the baseRowId.

### -param pageRecordCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of records in a desired record page

### -param baseRowId

Type: **[INT64](/windows/desktop/winprog/windows-data-types)**
Filters out new records by returning only records with rowId value less than or equal to baseRowId (this is useful if querying code wants to limit results to only events that were available at the time of DdqGetDiagnosticRecordStats call. The maxRowId parameter can be used as baseRowId). No filtering is applied if –1 is passed for baseRowId.

### -param hRecord

Type: **[HANDLE\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the handle for the resource that contains the list of matching records.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

