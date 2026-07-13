---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordProducerAtIndex
title: DdqGetDiagnosticRecordProducerAtIndex
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordProducerAtIndex
description: Fetches the description of a producer at the specified index in the resource pointed to by the HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION handle.
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
 - DdqGetDiagnosticRecordProducerAtIndex
f1_keywords:
 - DdqGetDiagnosticRecordProducerAtIndex
 - diagnosticdataquery/DdqGetDiagnosticRecordProducerAtIndex
---

## -description

Fetches the description of a producer at the specified index in the resource pointed to by the HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION handle.

## -parameters

### -param hProducerDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains set of producers.

### -param index

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The index of the producer to fetch.

### -param producerDescription

Type: **[DIAGNOSTIC_DATA_EVENT_PRODUCER_DESCRIPTION\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description)**
This output parameter is the pointer to the resource that describes the fetched producer.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See **[DIAGNOSTIC_DATA_EVENT_PRODUCER_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description.md)** for documentation on how a producer is defined.

## -see-also