---
UID: NF:diagnosticdataquery.DdqFreeDiagnosticRecordPage
title: DdqFreeDiagnosticRecordPage
ms.date: 8/19/2019
ms.keywords: DdqFreeDiagnosticRecordPage
description: Frees memory allocated for the diagnostic record page referenced by HDIAGNOSTIC_RECORD handle.
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
 - DdqFreeDiagnosticRecordPage
f1_keywords:
 - DdqFreeDiagnosticRecordPage
 - diagnosticdataquery/DdqFreeDiagnosticRecordPage
---

## -description

Frees memory allocated for the diagnostic record page referenced by HDIAGNOSTIC_RECORD handle.

## -parameters

### -param hRecord

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the set of diagnostic records to be freed.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more information about the DIAGNOSTIC_RECORD datatype, see [**here**](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_record.md).

## -see-also
