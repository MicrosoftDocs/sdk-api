---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordProducers
title: DdqGetDiagnosticRecordProducers
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordProducers
description: Fetches Diagnostic Data Producers available for a Diagnostic Data Query session.
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
 - DdqGetDiagnosticRecordProducers
f1_keywords:
 - DdqGetDiagnosticRecordProducers
 - diagnosticdataquery/DdqGetDiagnosticRecordProducers
---

## -description

Fetches Diagnostic Data Producers available for a Diagnostic Data Query session.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param hProducerDescription

Type: **[HANDLE\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the handle for the resource that contains the list of producers.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See **[DIAGNOSTIC_DATA_EVENT_PRODUCER_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description.md)** for documentation on how a producer is defined.

## -see-also