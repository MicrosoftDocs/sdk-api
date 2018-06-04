---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



