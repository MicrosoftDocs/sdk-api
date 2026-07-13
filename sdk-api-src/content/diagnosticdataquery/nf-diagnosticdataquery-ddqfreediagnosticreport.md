---
UID: NF:diagnosticdataquery.DdqFreeDiagnosticReport
title: DdqFreeDiagnosticReport
ms.date: 8/19/2019
ms.keywords: DdqFreeDiagnosticReport
description: Frees memory allocated for error reports referenced by HDIAGNOSTIC_REPORT_DATA handle.
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
 - DdqFreeDiagnosticReport
f1_keywords:
 - DdqFreeDiagnosticReport
 - diagnosticdataquery/DdqFreeDiagnosticReport
---

## -description

Frees memory allocated for error reports referenced by HDIAGNOSTIC_REPORT_DATA handle.

## -parameters

### -param hReport

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
The handle to the resource that contains the set of error reports to be freed.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For information the datatype DIAGNOSTIC_REPORT_DATA, see [**here**](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_report_data)

## -see-also

