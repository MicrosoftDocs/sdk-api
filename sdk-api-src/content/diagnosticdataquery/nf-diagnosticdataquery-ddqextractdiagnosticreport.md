---
UID: NF:diagnosticdataquery.DdqExtractDiagnosticReport
title: DdqExtractDiagnosticReport
ms.date: 8/19/2019
ms.keywords: DdqExtractDiagnosticReport
description: Used for retrieving Windows Error Reporting reports, this API extracts cabs to destination path specified. If the error report does not contain any cabs, no work is performed.
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
 - DdqExtractDiagnosticReport
f1_keywords:
 - DdqExtractDiagnosticReport
 - diagnosticdataquery/DdqExtractDiagnosticReport
---

## -description

Used for retrieving Windows Error Reporting reports, this API extracts cabs to destination path specified. If the error report does not contain any cabs, no work is performed.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the current Diagnostic Data Query session

### -param reportStoreType

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The type of report store to extract from. See remarks.

### -param reportKey

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
A pointer to the report key string. See remarks.

### -param destinationPath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
The destination path the report should be extracted to.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For report store types, see the [**WER APIs**](/windows/win32/api/werapi/nf-werapi-werstoreopen).
For report keys, see the [**WER APIs**](/windows/win32/api/werapi/nf-werapi-werstoregetnextreportkey).

## -see-also

