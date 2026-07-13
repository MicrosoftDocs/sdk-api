---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordProducerCount
title: DdqGetDiagnosticRecordProducerCount
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordProducerCount
description: Fetches the number (size) of producers in the resource pointed to by the HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION.
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
 - DdqGetDiagnosticRecordProducerCount
f1_keywords:
 - DdqGetDiagnosticRecordProducerCount
 - diagnosticdataquery/DdqGetDiagnosticRecordProducerCount
---

## -description

Fetches the number (size) of producers in the resource pointed to by the HDIAGNOSTIC_EVENT_PRODUCER_DESCRIPTION.

## -parameters

### -param hProducerDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains list of producers.

### -param producerDescriptionCount

Type: **[UNINT32\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the number of producers in provided resource.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See **[DIAGNOSTIC_DATA_EVENT_PRODUCER_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_producer_description.md)** for documentation on how a producer is defined.

## -see-also