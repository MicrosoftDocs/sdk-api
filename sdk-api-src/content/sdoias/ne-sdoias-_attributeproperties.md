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

# _ATTRIBUTEPROPERTIES enumeration


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

Used by filter configuration attributes <a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">MS_ATTRIBUTE_FILTER</a> and <a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">MS_ATTRIBUTE_QUARANTINE_IPFILTER</a>. See MS-Filter section in <a href="Http://go.microsoft.com/fwlink/p/?linkid=90366">RFC 2548</a> for more information.


## -remarks



The 
<a href="https://msdn.microsoft.com/47da09d8-9b45-4910-a6b1-1759c5000482">DICTIONARYPROPERTIES</a> enumeration type contains the attributes collection property, <b>PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION</b>.




## -see-also




<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>



<a href="https://msdn.microsoft.com/50d56c43-6552-4bb0-a204-a0cfc3ee7202">ATTRIBUTESYNTAX</a>



<a href="https://msdn.microsoft.com/47da09d8-9b45-4910-a6b1-1759c5000482">DICTIONARYPROPERTIES</a>
 

 

