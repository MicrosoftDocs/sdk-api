---
UID: NF:diagnosticdataquery.DdqGetTranscriptConfiguration
title: DdqGetTranscriptConfiguration
ms.date: 8/19/2019
ms.keywords: DdqGetTranscriptConfiguration
description: Gets event transcript configuration, such as maximum storage size and hours of data history.
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
 - DdqGetTranscriptConfiguration
f1_keywords:
 - DdqGetTranscriptConfiguration
 - diagnosticdataquery/DdqGetTranscriptConfiguration
---

## -description

Gets event transcript configuration, such as maximum storage size hours of data history to keep.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param currentConfig

Type: **[DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION\*](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_transcript_configuration)**
This output parameter is a pointer to the resource that contains the event transcript configuration details.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

