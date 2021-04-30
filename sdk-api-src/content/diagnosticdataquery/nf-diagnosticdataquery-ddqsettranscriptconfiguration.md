---
UID: NF:diagnosticdataquery.DdqSetTranscriptConfiguration
title: DdqSetTranscriptConfiguration
ms.date: 8/19/2019
ms.keywords: DdqSetTranscriptConfiguration
description: Sets event transcript configuration, such as maximum storage size and hours of data history. Note that setting the configuration will fail if the user is not elevated.
ms.localizationpriority: low
tech.root: security
targetos: Windows
ms.prod: windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param desiredConfig

Type: **[DIAGNOSTIC_DATA_EVENT_TRANSCRIPT_CONFIGURATION\*](/windows/win32/api/diagnosticdataquery/ns-diagnosticdataquerytypes-diagnostic_data_event_transcript_configuration)**
Pointer to the resource that contains the desired event transcript configuration.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

