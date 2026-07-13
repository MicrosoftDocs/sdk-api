---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordPayload
title: DdqGetDiagnosticRecordPayload
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordPayload
description: Fetches the payload text for the event record specified by rowId.
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
 - DdqGetDiagnosticRecordPayload
f1_keywords:
 - DdqGetDiagnosticRecordPayload
 - diagnosticdataquery/DdqGetDiagnosticRecordPayload
---

## -description

Fetches the payload text for the event record specified by rowId.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param rowId

Type: **[INT64](/windows/desktop/winprog/windows-data-types)**
The row id for the event record of interest.

### -param payload

Type: **[PCWSTR\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the payload text.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

