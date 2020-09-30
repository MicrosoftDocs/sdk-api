---
UID: NF:diagnosticdataquery.DdqGetDiagnosticReportStoreReportCount
title: DdqGetDiagnosticReportStoreReportCount
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticReportStoreReportCount
ms.topic: language-reference
description: Fetches the number (size) of reports stored in the requested store.
ms.localizationpriority: low
tech.root: security
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - 
api_location:
 - diagnosticdataquery.h
api_name:
 - DdqGetDiagnosticReportStoreReportCount
f1_keywords:
 - DdqGetDiagnosticReportStoreReportCount
 - diagnosticdataquery/DdqGetDiagnosticReportStoreReportCount
---

## -description

Fetches the number (size) of reports stored in the requested store.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param reportStoreType

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The type of report store to extract from. See remarks.

### -param reportCount

Type: **[UINT32\*](/windows/desktop/com/structure-of-com-error-codes)**
Pointer to the number of error reports.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

