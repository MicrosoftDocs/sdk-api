---
UID: NE:propsys.PROPDESC_TYPE_FLAGS
title: PROPDESC_TYPE_FLAGS (propsys.h)
description: Describes attributes of the typeInfo element in the property's .propdesc file.
helpviewer_keywords: ["PDTF_CANBEPURGED","PDTF_CANGROUPBY","PDTF_CANSTACKBY","PDTF_DEFAULT","PDTF_INCLUDEINFULLTEXTQUERY","PDTF_ISGROUP","PDTF_ISINNATE","PDTF_ISQUERYABLE","PDTF_ISSYSTEMPROPERTY","PDTF_ISTREEPROPERTY","PDTF_ISVIEWABLE","PDTF_MASK_ALL","PDTF_MULTIPLEVALUES","PDTF_SEARCHRAWVALUE","PROPDESC_TYPE_FLAGS","PROPDESC_TYPE_FLAGS enumeration [Windows Properties]","properties.PROPDESC_TYPE_FLAGS","propsys/PDTF_CANBEPURGED","propsys/PDTF_CANGROUPBY","propsys/PDTF_CANSTACKBY","propsys/PDTF_DEFAULT","propsys/PDTF_INCLUDEINFULLTEXTQUERY","propsys/PDTF_ISGROUP","propsys/PDTF_ISINNATE","propsys/PDTF_ISQUERYABLE","propsys/PDTF_ISSYSTEMPROPERTY","propsys/PDTF_ISTREEPROPERTY","propsys/PDTF_ISVIEWABLE","propsys/PDTF_MASK_ALL","propsys/PDTF_MULTIPLEVALUES","propsys/PDTF_SEARCHRAWVALUE","propsys/PROPDESC_TYPE_FLAGS","shell.PROPDESC_TYPE_FLAGS","shell_PROPDESC_TYPE_FLAGS"]
old-location: properties\PROPDESC_TYPE_FLAGS.htm
tech.root: properties
ms.assetid: e8027e59-3d37-4cb9-b73b-b1f05a2f959b
ms.date: 12/05/2018
ms.keywords: PDTF_CANBEPURGED, PDTF_CANGROUPBY, PDTF_CANSTACKBY, PDTF_DEFAULT, PDTF_INCLUDEINFULLTEXTQUERY, PDTF_ISGROUP, PDTF_ISINNATE, PDTF_ISQUERYABLE, PDTF_ISSYSTEMPROPERTY, PDTF_ISTREEPROPERTY, PDTF_ISVIEWABLE, PDTF_MASK_ALL, PDTF_MULTIPLEVALUES, PDTF_SEARCHRAWVALUE, PROPDESC_TYPE_FLAGS, PROPDESC_TYPE_FLAGS enumeration [Windows Properties], properties.PROPDESC_TYPE_FLAGS, propsys/PDTF_CANBEPURGED, propsys/PDTF_CANGROUPBY, propsys/PDTF_CANSTACKBY, propsys/PDTF_DEFAULT, propsys/PDTF_INCLUDEINFULLTEXTQUERY, propsys/PDTF_ISGROUP, propsys/PDTF_ISINNATE, propsys/PDTF_ISQUERYABLE, propsys/PDTF_ISSYSTEMPROPERTY, propsys/PDTF_ISTREEPROPERTY, propsys/PDTF_ISVIEWABLE, propsys/PDTF_MASK_ALL, propsys/PDTF_MULTIPLEVALUES, propsys/PDTF_SEARCHRAWVALUE, propsys/PROPDESC_TYPE_FLAGS, shell.PROPDESC_TYPE_FLAGS, shell_PROPDESC_TYPE_FLAGS
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
req.typenames: PROPDESC_TYPE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_TYPE_FLAGS
 - propsys/PROPDESC_TYPE_FLAGS
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
 - PROPDESC_TYPE_FLAGS
---

# PROPDESC_TYPE_FLAGS enumeration


## -description

Describes attributes of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

## -enum-fields

### -field PDTF_DEFAULT:0

The property uses the default values for all attributes.

### -field PDTF_MULTIPLEVALUES:0x1

The property can have multiple values. These values are stored as a VT_VECTOR in the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. This value is set by the <i>multipleValues</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_ISINNATE:0x2

This flag indicates that a property is read-only, and cannot be written to. This value is set by the <i>isInnate</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_ISGROUP:0x4

The property is a group heading. This value is set by the <i>isGroup</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_CANGROUPBY:0x8

The user can group by this property. This value is set by the <i>canGroupBy</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_CANSTACKBY:0x10

The user can stack by this property. This value is set by the <i>canStackBy</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_ISTREEPROPERTY:0x20

This property contains a hierarchy. This value is set by the <i>isTreeProperty</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_INCLUDEINFULLTEXTQUERY:0x40

<b>Deprecated in Windows 7 and later</b>. Include this property in any full text query that is performed. This value is set by the <i>includeInFullTextQuery</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_ISVIEWABLE:0x80

This property is meant to be viewed by the user. This influences whether the property shows up in the "Choose Columns" dialog box, for example. This value is set by the <i>isViewable</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_ISQUERYABLE:0x100

<b>Deprecated in Windows 7 and later</b>. This property is included in the list of properties that can be queried. A queryable property must also be viewable. This influences whether the property shows up in the query builder UI. This value is set by the <i>isQueryable</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

### -field PDTF_CANBEPURGED:0x200

<b>Windows Vista with Service Pack 1 (SP1) and later</b>. Used with an innate property (that is, a value calculated from other property values) to indicate that it can be deleted. This value is used by the <b>Remove Properties</b> UI to determine whether to display a check box next to a property that enables that property to be selected for removal. Note that a property that is not innate can always be purged regardless of the presence or absence of this flag.

### -field PDTF_SEARCHRAWVALUE:0x400

<b>Windows 7 and later</b>. The unformatted (raw) property value should be used for searching.

### -field PDTF_DONTCOERCEEMPTYSTRINGS:0x800

### -field PDTF_ALWAYSINSUPPLEMENTALSTORE:0x1000

### -field PDTF_ISSYSTEMPROPERTY:0x80000000

This property is owned by the system.

### -field PDTF_MASK_ALL:0x80001fff

A mask used to retrieve all flags.

## -remarks

These values are defined in propsys.h and propsys.idl.
