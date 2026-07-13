---
UID: NF:diagnosticdataquery.DdqGetDiagnosticReport
title: DdqGetDiagnosticReport
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticReport
description: Fetches error reports uploaded or enqueued for upload from this PC via HDIAGNOSTIC_REPORT_DATA handle.
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
 - DdqGetDiagnosticReport
f1_keywords:
 - DdqGetDiagnosticReport
 - diagnosticdataquery/DdqGetDiagnosticReport
---

## -description

Fetches error reports uploaded or enqueued for upload from this PC via HDIAGNOSTIC_REPORT_DATA handle.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param reportStoreType

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The type of report store to extract from. See remarks.

### -param hReport

Type: **[HANDLE\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the handle for the resource that contains the known set of problem reports.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For report store types, see the [**WER APIs**](/windows/win32/api/werapi/nf-werapi-werstoreopen).

## -see-also

