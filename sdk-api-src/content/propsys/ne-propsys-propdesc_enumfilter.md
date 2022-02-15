---
UID: NE:propsys.PROPDESC_ENUMFILTER
title: PROPDESC_ENUMFILTER (propsys.h)
description: Describes the filtered list of property descriptions that is returned.
helpviewer_keywords: ["PDEF_ALL","PDEF_COLUMN","PDEF_INFULLTEXTQUERY","PDEF_NONSYSTEM","PDEF_QUERYABLE","PDEF_SYSTEM","PDEF_VIEWABLE","PROPDESC_ENUMFILTER","PROPDESC_ENUMFILTER enumeration [Windows Properties]","properties.PROPDESC_ENUMFILTER","propsys/PDEF_ALL","propsys/PDEF_COLUMN","propsys/PDEF_INFULLTEXTQUERY","propsys/PDEF_NONSYSTEM","propsys/PDEF_QUERYABLE","propsys/PDEF_SYSTEM","propsys/PDEF_VIEWABLE","propsys/PROPDESC_ENUMFILTER","shell.PROPDESC_ENUMFILTER","shell_PROPDESC_ENUMFILTER"]
old-location: properties\PROPDESC_ENUMFILTER.htm
tech.root: properties
ms.assetid: dae1fadc-d7ea-4cad-b441-0e5c9708f5ce
ms.date: 12/05/2018
ms.keywords: PDEF_ALL, PDEF_COLUMN, PDEF_INFULLTEXTQUERY, PDEF_NONSYSTEM, PDEF_QUERYABLE, PDEF_SYSTEM, PDEF_VIEWABLE, PROPDESC_ENUMFILTER, PROPDESC_ENUMFILTER enumeration [Windows Properties], properties.PROPDESC_ENUMFILTER, propsys/PDEF_ALL, propsys/PDEF_COLUMN, propsys/PDEF_INFULLTEXTQUERY, propsys/PDEF_NONSYSTEM, propsys/PDEF_QUERYABLE, propsys/PDEF_SYSTEM, propsys/PDEF_VIEWABLE, propsys/PROPDESC_ENUMFILTER, shell.PROPDESC_ENUMFILTER, shell_PROPDESC_ENUMFILTER
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPDESC_ENUMFILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_ENUMFILTER
 - propsys/PROPDESC_ENUMFILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_ENUMFILTER
---

# PROPDESC_ENUMFILTER enumeration


## -description

Describes the filtered list of property descriptions that is returned.

## -enum-fields

### -field PDEF_ALL:0

The list contains all property descriptions in the system.

### -field PDEF_SYSTEM:1

The list contains system property descriptions only. It excludes third-party property descriptions that are registered on the computer.

### -field PDEF_NONSYSTEM:2

The list contains only third-party property descriptions that are registered on the computer.

### -field PDEF_VIEWABLE:3

The list contains only viewable properties, where &lt;typeInfo isViewable="true"&gt;.

### -field PDEF_QUERYABLE:4

Deprecated in <b>Windows 7 and later</b>. The list contains only queryable properties, where &lt;typeInfo isViewable="true" isQueryable="true"&gt;.

### -field PDEF_INFULLTEXTQUERY:5

<b>Deprecated in Windows 7 and later</b>. The list contains only properties to be included in full-text queries.

### -field PDEF_COLUMN:6

The list contains only properties that are columns.

## -remarks

These values are defined in propsys.h and propsys.idl.

