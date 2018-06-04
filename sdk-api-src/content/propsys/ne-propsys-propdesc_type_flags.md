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

# PROPDESC_TYPE_FLAGS enumeration


## -description


Describes attributes of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


## -enum-fields




### -field PDTF_DEFAULT

The property uses the default values for all attributes.


### -field PDTF_MULTIPLEVALUES

The property can have multiple values. These values are stored as a VT_VECTOR in the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. This value is set by the <i>multipleValues</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_ISINNATE

This flag indicates that a property is read-only, and cannot be written to. This value is set by the <i>isInnate</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_ISGROUP

The property is a group heading. This value is set by the <i>isGroup</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_CANGROUPBY

The user can group by this property. This value is set by the <i>canGroupBy</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_CANSTACKBY

The user can stack by this property. This value is set by the <i>canStackBy</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_ISTREEPROPERTY

This property contains a hierarchy. This value is set by the <i>isTreeProperty</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_INCLUDEINFULLTEXTQUERY

<b>Deprecated in Windows 7 and later</b>. Include this property in any full text query that is performed. This value is set by the <i>includeInFullTextQuery</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_ISVIEWABLE

This property is meant to be viewed by the user. This influences whether the property shows up in the "Choose Columns" dialog box, for example. This value is set by the <i>isViewable</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_ISQUERYABLE

<b>Deprecated in Windows 7 and later</b>. This property is included in the list of properties that can be queried. A queryable property must also be viewable. This influences whether the property shows up in the query builder UI. This value is set by the <i>isQueryable</i> attribute of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.


### -field PDTF_CANBEPURGED

<b>Windows Vista with Service Pack 1 (SP1) and later</b>. Used with an innate property (that is, a value calculated from other property values) to indicate that it can be deleted. This value is used by the <b>Remove Properties</b> UI to determine whether to display a check box next to a property that enables that property to be selected for removal. Note that a property that is not innate can always be purged regardless of the presence or absence of this flag.


### -field PDTF_SEARCHRAWVALUE

<b>Windows 7 and later</b>. The unformatted (raw) property value should be used for searching.


### -field PDTF_DONTCOERCEEMPTYSTRINGS


### -field PDTF_ALWAYSINSUPPLEMENTALSTORE


### -field PDTF_ISSYSTEMPROPERTY

This property is owned by the system.


### -field PDTF_MASK_ALL

A mask used to retrieve all flags.


## -remarks



These values are defined in propsys.h and propsys.idl.



