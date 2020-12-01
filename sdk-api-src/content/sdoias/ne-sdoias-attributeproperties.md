---
UID: NE:sdoias._ATTRIBUTEPROPERTIES
title: ATTRIBUTEPROPERTIES (sdoias.h)
description: The values of the ATTRIBUTEPROPERTIES type enumerate properties for a RADIUS dictionary attribute.
helpviewer_keywords: ["ATTRIBUTEPROPERTIES","ATTRIBUTEPROPERTIES enumeration [Network Policy Server]","PROPERTY_ATTRIBUTE_ALLOW_IN_8021X","PROPERTY_ATTRIBUTE_ALLOW_IN_CONDITION","PROPERTY_ATTRIBUTE_ALLOW_IN_PROFILE","PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_CONDITION","PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_PROFILE","PROPERTY_ATTRIBUTE_ALLOW_IN_VPNDIALUP","PROPERTY_ATTRIBUTE_ALLOW_LOG_ORDINAL","PROPERTY_ATTRIBUTE_ALLOW_MULTIPLE","PROPERTY_ATTRIBUTE_DISPLAY_NAME","PROPERTY_ATTRIBUTE_ENUM_FILTERS","PROPERTY_ATTRIBUTE_ENUM_NAMES","PROPERTY_ATTRIBUTE_ENUM_VALUES","PROPERTY_ATTRIBUTE_ID","PROPERTY_ATTRIBUTE_IS_ENUMERABLE","PROPERTY_ATTRIBUTE_SYNTAX","PROPERTY_ATTRIBUTE_VALUE","PROPERTY_ATTRIBUTE_VENDOR_ID","PROPERTY_ATTRIBUTE_VENDOR_TYPE_ID","_sdo_attributeproperties","nps.SDO_attributeproperties","sdo.attributeproperties","sdoias/ATTRIBUTEPROPERTIES","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_8021X","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_CONDITION","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROFILE","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_CONDITION","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_PROFILE","sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_VPNDIALUP","sdoias/PROPERTY_ATTRIBUTE_ALLOW_LOG_ORDINAL","sdoias/PROPERTY_ATTRIBUTE_ALLOW_MULTIPLE","sdoias/PROPERTY_ATTRIBUTE_DISPLAY_NAME","sdoias/PROPERTY_ATTRIBUTE_ENUM_FILTERS","sdoias/PROPERTY_ATTRIBUTE_ENUM_NAMES","sdoias/PROPERTY_ATTRIBUTE_ENUM_VALUES","sdoias/PROPERTY_ATTRIBUTE_ID","sdoias/PROPERTY_ATTRIBUTE_IS_ENUMERABLE","sdoias/PROPERTY_ATTRIBUTE_SYNTAX","sdoias/PROPERTY_ATTRIBUTE_VALUE","sdoias/PROPERTY_ATTRIBUTE_VENDOR_ID","sdoias/PROPERTY_ATTRIBUTE_VENDOR_TYPE_ID"]
old-location: nps\SDO_attributeproperties.htm
tech.root: Nps
ms.assetid: eb8cff95-4ea3-446c-893f-3065d3a037d3
ms.date: 12/05/2018
ms.keywords: ATTRIBUTEPROPERTIES, ATTRIBUTEPROPERTIES enumeration [Network Policy Server], PROPERTY_ATTRIBUTE_ALLOW_IN_8021X, PROPERTY_ATTRIBUTE_ALLOW_IN_CONDITION, PROPERTY_ATTRIBUTE_ALLOW_IN_PROFILE, PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_CONDITION, PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_PROFILE, PROPERTY_ATTRIBUTE_ALLOW_IN_VPNDIALUP, PROPERTY_ATTRIBUTE_ALLOW_LOG_ORDINAL, PROPERTY_ATTRIBUTE_ALLOW_MULTIPLE, PROPERTY_ATTRIBUTE_DISPLAY_NAME, PROPERTY_ATTRIBUTE_ENUM_FILTERS, PROPERTY_ATTRIBUTE_ENUM_NAMES, PROPERTY_ATTRIBUTE_ENUM_VALUES, PROPERTY_ATTRIBUTE_ID, PROPERTY_ATTRIBUTE_IS_ENUMERABLE, PROPERTY_ATTRIBUTE_SYNTAX, PROPERTY_ATTRIBUTE_VALUE, PROPERTY_ATTRIBUTE_VENDOR_ID, PROPERTY_ATTRIBUTE_VENDOR_TYPE_ID, _sdo_attributeproperties, nps.SDO_attributeproperties, sdo.attributeproperties, sdoias/ATTRIBUTEPROPERTIES, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_8021X, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_CONDITION, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROFILE, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_CONDITION, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_PROFILE, sdoias/PROPERTY_ATTRIBUTE_ALLOW_IN_VPNDIALUP, sdoias/PROPERTY_ATTRIBUTE_ALLOW_LOG_ORDINAL, sdoias/PROPERTY_ATTRIBUTE_ALLOW_MULTIPLE, sdoias/PROPERTY_ATTRIBUTE_DISPLAY_NAME, sdoias/PROPERTY_ATTRIBUTE_ENUM_FILTERS, sdoias/PROPERTY_ATTRIBUTE_ENUM_NAMES, sdoias/PROPERTY_ATTRIBUTE_ENUM_VALUES, sdoias/PROPERTY_ATTRIBUTE_ID, sdoias/PROPERTY_ATTRIBUTE_IS_ENUMERABLE, sdoias/PROPERTY_ATTRIBUTE_SYNTAX, sdoias/PROPERTY_ATTRIBUTE_VALUE, sdoias/PROPERTY_ATTRIBUTE_VENDOR_ID, sdoias/PROPERTY_ATTRIBUTE_VENDOR_TYPE_ID
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ATTRIBUTEPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ATTRIBUTEPROPERTIES
 - sdoias/_ATTRIBUTEPROPERTIES
 - ATTRIBUTEPROPERTIES
 - sdoias/ATTRIBUTEPROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - ATTRIBUTEPROPERTIES
---

# ATTRIBUTEPROPERTIES enumeration


## -description

The values of the 
<b>ATTRIBUTEPROPERTIES</b> type enumerate properties for a RADIUS dictionary attribute.

## -enum-fields

### -field PROPERTY_ATTRIBUTE_ID

The ID of the attribute.

### -field PROPERTY_ATTRIBUTE_VENDOR_ID

The vendor ID for Vendor Specific Attributes (VSA).

### -field PROPERTY_ATTRIBUTE_VENDOR_TYPE_ID

The vendor-specific type ID for Vendor Specific Attributes (VSA).

### -field PROPERTY_ATTRIBUTE_IS_ENUMERABLE

Specifies whether the attribute is enumerable.

### -field PROPERTY_ATTRIBUTE_ENUM_NAMES

The IDs for an enumerable attribute.

### -field PROPERTY_ATTRIBUTE_ENUM_VALUES

The values for an enumerable attribute.

### -field PROPERTY_ATTRIBUTE_SYNTAX

Specifies the syntax of the attribute.

### -field PROPERTY_ATTRIBUTE_ALLOW_MULTIPLE

Specifies whether multiple instances of this attribute are allowed.

### -field PROPERTY_ATTRIBUTE_ALLOW_LOG_ORDINAL

Specifies the Open Database Connectivity (ODBC) ordinal.

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_PROFILE

Specifies whether this attribute is allowed in the profile for a Network Access Policy (NAP).

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_CONDITION

Specifies whether this attribute is allowed in a condition for a Network Access Policy (NAP).

### -field PROPERTY_ATTRIBUTE_DISPLAY_NAME

The display name for the attribute.

### -field PROPERTY_ATTRIBUTE_VALUE

Specifies the value for the attribute.

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_PROFILE

Specifies whether the attribute is allowed in an NAP profile for a network request proxy.

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_PROXY_CONDITION

Specifies whether the attribute is allowed in an NAP condition for a network request proxy.

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_VPNDIALUP

Used by NPS user interface to mark whether an attribute is used in profiles for VPN scenario.

### -field PROPERTY_ATTRIBUTE_ALLOW_IN_8021X

Used by NPS user interface to mark whether an attribute is used in profiles for 802.1X scenario.

### -field PROPERTY_ATTRIBUTE_ENUM_FILTERS

Used by filter configuration attributes <a href="/windows/desktop/api/sdoias/ne-sdoias-attributeid">MS_ATTRIBUTE_FILTER</a> and <a href="/windows/desktop/api/sdoias/ne-sdoias-attributeid">MS_ATTRIBUTE_QUARANTINE_IPFILTER</a>. See MS-Filter section in <a href="https://www.ietf.org/rfc/rfc2548.txt">RFC 2548</a> for more information.

## -remarks

The 
<a href="/windows/desktop/api/sdoias/ne-sdoias-dictionaryproperties">DICTIONARYPROPERTIES</a> enumeration type contains the attributes collection property, <b>PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION</b>.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-attributeid">ATTRIBUTEID</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-attributesyntax">ATTRIBUTESYNTAX</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-dictionaryproperties">DICTIONARYPROPERTIES</a>