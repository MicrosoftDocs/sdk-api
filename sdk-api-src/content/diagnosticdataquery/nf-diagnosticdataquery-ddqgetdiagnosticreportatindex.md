---
UID: NF:diagnosticdataquery.DdqGetDiagnosticReportAtIndex
title: DdqGetDiagnosticReportAtIndex
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticReportAtIndex
description: Fetches an error report and its information at the specified index in the resource pointed to by the HDIAGNOSTIC_REPORT_DATA handle.
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
 - DdqGetDiagnosticReportAtIndex
f1_keywords:
 - DdqGetDiagnosticReportAtIndex
 - diagnosticdataquery/DdqGetDiagnosticReportAtIndex
---

## -description

Fetches an error report and its information at the specified index in the resource pointed to by the HDIAGNOSTIC_REPORT_DATA handle.

## -parameters

### -param hReport

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource with the set of problem reports.

### -param index

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The index of the error report to fetch.

### -param report

Type: **[DIAGNOSTIC_DATA_REPORT_DATA\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_report_data)**
This output parameter is a pointer to the resource that contains information about the fetched diagnostic report.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

