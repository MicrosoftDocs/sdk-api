---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordCount
title: DdqGetDiagnosticRecordCount
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordCount
description: Fetches number (size) of elements in the resource pointed to by the HDIAGNOSTIC_DATA_RECORD handle.
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
 - DdqGetDiagnosticRecordCount
f1_keywords:
 - DdqGetDiagnosticRecordCount
 - diagnosticdataquery/DdqGetDiagnosticRecordCount
---

## -description

Fetches number (size) of diagnostic records in the resource pointed to by the HDIAGNOSTIC_DATA_RECORD handle.

## -parameters

### -param hRecord

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the DIAGNOSTIC_DATA_RECORD list.

### -param recordCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Number of items in the DIAGNOSTIC_DATA_RECORD list.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more information about diagnostic data record data type, see [**DIAGNOSTIC_DATA_RECORD**](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_record.md)

## -see-also