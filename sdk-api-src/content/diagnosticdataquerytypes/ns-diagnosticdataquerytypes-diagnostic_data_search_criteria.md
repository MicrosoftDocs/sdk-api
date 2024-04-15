---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_SEARCH_CRITERIA
title: DIAGNOSTIC_DATA_SEARCH_CRITERIA
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_SEARCH_CRITERIA, DIAGNOSTIC_DATA_SEARCH_CRITERIA
description: This resource contains details of the search criteria when fetching a diagnostic data record.
tech.root: security
targetos: Windows
ms.service: windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquerytypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: DIAGNOSTIC_DATA_SEARCH_CRITERIA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_SEARCH_CRITERIA
 - DIAGNOSTIC_DATA_SEARCH_CRITERIA
f1_keywords:
 - tagDIAGNOSTIC_DATA_SEARCH_CRITERIA
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_SEARCH_CRITERIA
 - DIAGNOSTIC_DATA_SEARCH_CRITERIA
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_SEARCH_CRITERIA
---

## -description

This resource contains details of the search criteria when fetching a diagnostic data record.

## -struct-fields

### -field producerNames

Type: **[LPCWSTR\*](/windows/desktop/winprog/windows-data-types)**
List of producer names to search for. A diagnostic data record that matches at least one of the producer names is included as a result in this search criteria. Use `nullptr` for this value to indicate no filter by producers.

### -field producerNameCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of producer names in the list of producer names to search for. Use `0` for this value to indicate no filter by producers.

### -field textToMatch

Type: **[LPCWSTR](/windows/desktop/winprog/windows-data-types)**
The sub-string to search for within diagnostic data records. This text is case insensitive.

### -field categoryIds

Type: **[INT32\*](/windows/desktop/winprog/windows-data-types)**
List of category identifiers to search for. A diagnostic data record that matches at least one of the category names is included as a result in this search criteria. Use `nullptr` for this value to indicate no filter by categories.

### -field categoryIdCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of categories in the list of category identifiers. Use `0` for this value to indicate no filter by categories.

### -field privacyTags

Type: **[INT32\*](/windows/desktop/winprog/windows-data-types)**
List of privacy tag identifiers to search for. A diagnostic data record that matches at least one of the tags is included as a result in this search criteria. Use `nullptr` for this value to indicate no filter by privacy tags.

### -field privacyTagCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of privacy tags in the list of privacy tag identifiers. Use `0` for this value to indicate no filter by tags.

### -field coreDataOnly

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**
`TRUE` to filter search results to only core data. `FALSE` to return both core and non-core data.

## -remarks

For more details on how core data is defined, see our [**privacy statement**](/windows/privacy/windows-diagnostic-data).

## -see-also

