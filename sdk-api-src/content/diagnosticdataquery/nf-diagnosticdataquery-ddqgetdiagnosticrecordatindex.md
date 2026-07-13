---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordAtIndex
title: DdqGetDiagnosticRecordAtIndex
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordAtIndex
description: Fetches diagnostic data record information at the specified index in the resource pointed to by the HDIAGNOSTIC_DATA_RECORD handle.
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
 - DdqGetDiagnosticRecordAtIndex
f1_keywords:
 - DdqGetDiagnosticRecordAtIndex
 - diagnosticdataquery/DdqGetDiagnosticRecordAtIndex
---

## -description

Fetches diagnostic data record information at the specified index in the resource pointed to by the HDIAGNOSTIC_DATA_RECORD handle.

## -parameters

### -param hRecord

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the list of DIAGNOSTIC_DATA_RECORD items.

### -param index

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Index of the record to be fetched.

### -param record

Type: **[DIAGNOSTIC_DATA_RECORD\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_record)**
This output parameter is a pointer to the record at the specified index.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

