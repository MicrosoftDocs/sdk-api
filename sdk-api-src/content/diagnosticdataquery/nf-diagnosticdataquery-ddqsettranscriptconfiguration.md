---
UID: NF:diagnosticdataquery.DdqSetTranscriptConfiguration
title: DdqSetTranscriptConfiguration
ms.date: 02/13/2023
ms.keywords: DdqSetTranscriptConfiguration
description: Sets event transcript configuration, such as maximum storage size and hours of data history. Note that setting the configuration will fail if the user is not elevated.
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
 - DdqSetTranscriptConfiguration
f1_keywords:
 - DdqSetTranscriptConfiguration
 - diagnosticdataquery/DdqSetTranscriptConfiguration
---

## -description

Sets event transcript configuration, such as maximum storage size and hours of data history. Note that setting the configuration will fail if the user is not elevated.

## -parameters

### -param hSession

A [HANDLE](/windows/win32/winprog/windows-data-types) to the **Diagnostic Data Query** session.

### -param desiredConfig

A [DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_transcript_configuration) that points to the resource that contains the desired event transcript configuration.

## -returns

An [HRESULT](/windows/win32/com/structure-of-com-error-codes) which returns `S_OK` on successful completion.

## -remarks

## -see-also
