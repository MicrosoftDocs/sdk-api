---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordProducerCategories
title: DdqGetDiagnosticRecordProducerCategories
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordProducerCategories
description: Producers and categories have a hierarchical relationship--that is, categories belong to producers. This function fetches the available Category IDs and text representation of categories for a given diagnostic Producer Name.
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
 - DdqGetDiagnosticRecordProducerCategories
f1_keywords:
 - DdqGetDiagnosticRecordProducerCategories
 - diagnosticdataquery/DdqGetDiagnosticRecordProducerCategories
---

## -description

Producers and categories have a hierarchical relationship--that is, categories belong to producers. This function fetches the available Category IDs and text representation of categories for a given diagnostic Producer Name.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param producerName

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
The name of the producer of interest.

### -param hCategoryDescription

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the resource that contains the list of categories and their descriptions that belong to the given producer.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

See **[DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_category_description.md)** for documentation on how a category is defined.

## -see-also
