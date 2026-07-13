---
UID: NF:diagnosticdataquery.DdqCancelDiagnosticRecordOperation
title: DdqCancelDiagnosticRecordOperation
ms.date: 8/19/2019
ms.keywords: DdqCancelDiagnosticRecordOperation
description: Cancels all outstanding Diagnostic Data Query API internal query operations for this session. This can be called from another thread to interrupt long running Query APIs.
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
 - DdqCancelDiagnosticRecordOperation
f1_keywords:
 - DdqCancelDiagnosticRecordOperation
 - diagnosticdataquery/DdqCancelDiagnosticRecordOperation
---

## -description

Cancels all outstanding Diagnostic Data Query API internal query operations for this session. This can be called from another thread to interrupt long running Query APIs.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

