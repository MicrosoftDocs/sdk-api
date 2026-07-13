---
UID: NF:diagnosticdataquery.DdqIsDiagnosticRecordSampledIn
title: DdqIsDiagnosticRecordSampledIn
ms.date: 8/19/2019
ms.keywords: DdqIsDiagnosticRecordSampledIn
description: Fetches the sampled-in state of the device for an event.
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
 - DdqIsDiagnosticRecordSampledIn
f1_keywords:
 - DdqIsDiagnosticRecordSampledIn
 - diagnosticdataquery/DdqIsDiagnosticRecordSampledIn
---

## -description

Fetches the sampled-in state of the device for an event.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param providerGroup

Type: **[GUID\*](../guiddef/ns-guiddef-guid.md)**
Pointer to the provider group GUID.

### -param providerId

Type: **[GUID\*](../guiddef/ns-guiddef-guid.md)**
Pointer to the provider GUID.

### -param providerName

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**
The name of the provider.

### -param eventId

Type: **[UNI32\*](/windows/win32/winprog/windows-data-types)**
Pointer to the event ID.

### -param eventName

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**
The name of the event.

### -param eventVersion

Type: **[UINT32\*](/windows/win32/winprog/windows-data-types)**
The version of the event.

### -param eventKeywords

Type: **[UINT64\*](/windows/win32/winprog/windows-data-types)**
Pointer to the event keywords.

### -param isSampledIn

Type: **[BOOL\*](/windows/win32/winprog/windows-data-types)**
This output parameter is a pointer to a boolean value that is TRUE if the event is sampled in and FALSE otherwise.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more information about events and providers, see [**Event Tracing**](/windows/win32/etw/event-tracing-portal).

## -see-also
