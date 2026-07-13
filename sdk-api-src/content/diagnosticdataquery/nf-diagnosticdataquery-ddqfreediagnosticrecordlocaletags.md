---
UID: NF:diagnosticdataquery.DdqFreeDiagnosticRecordLocaleTags
title: DdqFreeDiagnosticRecordLocaleTags
ms.date: 8/19/2019
ms.keywords: DdqFreeDiagnosticRecordLocaleTags
description: Frees memory allocated for tag information referenced by HDIAGNOSTIC_EVENT_TAG_DESCRIPTION handle.
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
 - DdqFreeDiagnosticRecordLocaleTags
f1_keywords:
 - DdqFreeDiagnosticRecordLocaleTags
 - diagnosticdataquery/DdqFreeDiagnosticRecordLocaleTags
---

## -description

Frees memory allocated for tag information referenced by HDIAGNOSTIC_EVENT_TAG_DESCRIPTION handle.

## -parameters

### -param hTagDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the tag descriptions being freed.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more details about the tag description data type, see our [**DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION**](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_tag_description).

## -see-also

