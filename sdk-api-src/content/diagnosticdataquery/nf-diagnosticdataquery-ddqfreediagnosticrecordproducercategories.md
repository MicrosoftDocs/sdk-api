---
UID: NF:diagnosticdataquery.DdqFreeDiagnosticRecordProducerCategories
title: DdqFreeDiagnosticRecordProducerCategories
ms.date: 8/19/2019
ms.keywords: DdqFreeDiagnosticRecordProducerCategories
description: Frees memory allocated for set of categories and the text representation of the categories referenced by HDIAGNOSTIC_EVENT_CATEGORY_DESCRIPTION handle.
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
 - DdqFreeDiagnosticRecordProducerCategories
f1_keywords:
 - DdqFreeDiagnosticRecordProducerCategories
 - diagnosticdataquery/DdqFreeDiagnosticRecordProducerCategories
---

## -description

Frees memory allocated for set of categories and the text representation of the categories referenced by HDIAGNOSTIC_EVENT_CATEGORY_DESCRIPTION handle.

## -parameters

### -param hCategoryDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the set of categories and their descriptions to be freed.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

For more information about the data type DIAGNOSTIC_EVENT_CATEGORY_DESCRIPTION, see [**here**](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_category_description.md).

## -see-also