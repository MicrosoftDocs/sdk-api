---
UID: NE:propsys.PROPDESC_ENUMFILTER
title: PROPDESC_ENUMFILTER
author: windows-driver-content
description: Describes the filtered list of property descriptions that is returned.
old-location: properties\PROPDESC_ENUMFILTER.htm
old-project: properties
ms.assetid: dae1fadc-d7ea-4cad-b441-0e5c9708f5ce
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: PDEF_ALL, PDEF_COLUMN, PDEF_INFULLTEXTQUERY, PDEF_NONSYSTEM, PDEF_QUERYABLE, PDEF_SYSTEM, PDEF_VIEWABLE, PROPDESC_ENUMFILTER, PROPDESC_ENUMFILTER enumeration [Windows Properties], properties.PROPDESC_ENUMFILTER, propsys/PDEF_ALL, propsys/PDEF_COLUMN, propsys/PDEF_INFULLTEXTQUERY, propsys/PDEF_NONSYSTEM, propsys/PDEF_QUERYABLE, propsys/PDEF_SYSTEM, propsys/PDEF_VIEWABLE, propsys/PROPDESC_ENUMFILTER, shell.PROPDESC_ENUMFILTER, shell_PROPDESC_ENUMFILTER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PROPDESC_ENUMFILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propsys.h
api_name:
-	PROPDESC_ENUMFILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PROPDESC_ENUMFILTER enumeration


## -description


Describes the filtered list of property descriptions that is returned.


## -enum-fields




### -field PDEF_ALL

The list contains all property descriptions in the system.


### -field PDEF_SYSTEM

The list contains system property descriptions only. It excludes third-party property descriptions that are registered on the computer.


### -field PDEF_NONSYSTEM

The list contains only third-party property descriptions that are registered on the computer.


### -field PDEF_VIEWABLE

The list contains only viewable properties, where &lt;typeInfo isViewable="true"&gt;.


### -field PDEF_QUERYABLE

Deprecated in <b>Windows 7 and later</b>. The list contains only queryable properties, where &lt;typeInfo isViewable="true" isQueryable="true"&gt;.


### -field PDEF_INFULLTEXTQUERY

<b>Deprecated in Windows 7 and later</b>. The list contains only properties to be included in full-text queries.


### -field PDEF_COLUMN

The list contains only properties that are columns.


## -remarks



These values are defined in propsys.h and propsys.idl.



