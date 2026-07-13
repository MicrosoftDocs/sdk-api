---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordCategoryAtIndex
title: DdqGetDiagnosticRecordCategoryAtIndex
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordCategoryAtIndex
description: Fetches a diagnostic record category at the specified index in the resource pointed to by the HDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION handle.
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
 - DdqGetDiagnosticRecordCategoryAtIndex
f1_keywords:
 - DdqGetDiagnosticRecordCategoryAtIndex
 - diagnosticdataquery/DdqGetDiagnosticRecordCategoryAtIndex
---

## -description

Fetches a diagnostic record category at the specified index in the resource pointed to bythe HDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION handle.

## -parameters

### -param hCategoryDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the list of categories and their descriptions

### -param index

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The index of the category to be fetched.

### -param categoryDescription

Type: **[DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_category_description.md)**
This outpoint parameter is a pointer to the category and its description that was fetched.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See **[DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_category_description.md)** for documentation on how a category is defined.

## -see-also