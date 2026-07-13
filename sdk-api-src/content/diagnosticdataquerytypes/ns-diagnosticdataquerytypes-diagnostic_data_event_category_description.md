---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
title: DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION, DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
description: A resource that represents a category, defined by an identifier and a name. A category is an organizational construct to categorize records for a given producer. For example, "Browsing Data" could be a category for the producer "Microsoft Edge".
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
req.typenames: DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
 - DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
f1_keywords:
 - tagDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
 - DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_EVENT_CATEGORY_DESCRIPTION
---

## -description

A resource that represents a category, defined by an identifier and a name. A category is an organizational construct to categorize records for a given producer. For example, "Browsing Data" could be a category for the producer "Microsoft Edge".

## -struct-fields

### -field id

Type: **[INT32](/windows/desktop/winprog/windows-data-types)**
An identifier to identify this category.

### -field name

Type: **[LPWSTR](/windows/desktop/winprog/windows-data-types)**
The name of this category.

## -remarks

## -see-also
