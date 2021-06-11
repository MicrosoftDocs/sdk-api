---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
title: DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION, DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
description: A resource that describes a tag, defined by the tag's name and its description.
tech.root: security
targetos: Windows
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
req.typenames: DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
 - DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
f1_keywords:
 - tagDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
 - diagnosticdataquerytypes/tagDIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
 - DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
 - diagnosticdataquerytypes/DIAGNOSTIC_DATA_EVENT_TAG_DESCRIPTION
---

## -description

A resource that describes a tag, defined by the tag's name and its description.

## -struct-fields

### -field privacyTag

Type: **[INT32](/windows/desktop/winprog/windows-data-types)**
A unique identifier for this tag.

### -field name

Type: **[LPWSTR](/windows/desktop/winprog/windows-data-types)**
The name of this tag.

### -field description

Type: **[LPWSTR](/windows/desktop/winprog/windows-data-types)**
The official description for this tag.

## -remarks

For more details, see our [**privacy statement**](/windows/privacy/windows-diagnostic-data).

## -see-also

