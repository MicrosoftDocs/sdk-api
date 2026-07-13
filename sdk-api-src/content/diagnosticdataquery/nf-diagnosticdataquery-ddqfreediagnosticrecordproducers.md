---
UID: NF:diagnosticdataquery.DdqFreeDiagnosticRecordProducers
title: DdqFreeDiagnosticRecordProducers
ms.date: 8/19/2019
ms.keywords: DdqFreeDiagnosticRecordProducers
description: Frees memory allocated for the set of producers referenced by HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION handle.
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
 - DdqFreeDiagnosticRecordProducers
f1_keywords:
 - DdqFreeDiagnosticRecordProducers
 - diagnosticdataquery/DdqFreeDiagnosticRecordProducers
---

## -description

Frees memory allocated for the set of producers referenced by HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION handle.

## -parameters

### -param hProducerDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the set of producers to be freed.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For information about the data type DIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION, see [**here**](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description)

## -see-also

