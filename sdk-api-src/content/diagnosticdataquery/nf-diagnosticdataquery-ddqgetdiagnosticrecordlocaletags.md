---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordLocaleTags
title: DdqGetDiagnosticRecordLocaleTags
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordLocaleTags
description: "Fetches information for all known tags under the specified locale and provides a handle, HDIAGNOSTIC_EVENT_TAG_DESCRIPTION, to the data. An example locale would be “en-US”. An example return value is a DIAGNOSTIC_EVENT_TAG_DESCRIPTION resource that contains the following data: tag: 11, name: “Device Connectivity and Configuration” and description: “Data that describes the connections and configuration of the devices connected to the service and the network, including device identifiers (e.g IP addresses) configuration, setting and performance”."
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
 - DdqGetDiagnosticRecordLocaleTags
f1_keywords:
 - DdqGetDiagnosticRecordLocaleTags
 - diagnosticdataquery/DdqGetDiagnosticRecordLocaleTags
---

## -description

Fetches information for all known tags under the specified locale and provides a handle, HDIAGNOSTIC_EVENT_TAG_DESCRIPTION, to the data. An example locale would be “en-US”. An example return value is a DIAGNOSTIC_EVENT_TAG_DESCRIPTION resource that contains the following data: tag: 11, name: “Device Connectivity and Configuration” and description: “Data that describes the connections and configuration of the devices connected to the service and the network, including device identifiers (e.g IP addresses) configuration, setting and performance”.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param locale

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
The locale for the tag descriptions.

### -param hTagDescription

Type: **[HANDLE\*](/windows/desktop/winprog/windows-data-types)**
This output parameter is a pointer to the handle for the resource that contains the list of tag descriptions. The resource is of the form DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION and contains the tag name, description and the numeric tag value.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more details about the tag description data type, see our [**DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION**](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_tag_description).

## -see-also

