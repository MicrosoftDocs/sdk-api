---
UID: NE:sdoias._ATTRIBUTEINFO
title: "_ATTRIBUTEINFO"
author: windows-driver-content
description: The values of the ATTRIBUTEINFO type enumerate characteristics of a specified attribute.
old-location: nps\SDO_attributeinfo.htm
old-project: Nps
ms.assetid: 84ed435c-c6e8-41e7-9a5f-acd78fce4a10
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ATTRIBUTEINFO, ATTRIBUTEINFO enumeration [Network Policy Server], DESCRIPTION, LDAPNAME, NAME, RESTRICTIONS, SYNTAX, VENDORID, VENDORTYPE, _ATTRIBUTEINFO, _sdo_attributeinfo, nps.SDO_attributeinfo, sdo.attributeinfo, sdoias/ATTRIBUTEINFO, sdoias/DESCRIPTION, sdoias/LDAPNAME, sdoias/NAME, sdoias/RESTRICTIONS, sdoias/SYNTAX, sdoias/VENDORID, sdoias/VENDORTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ATTRIBUTEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SdoIas.h
api_name:
-	ATTRIBUTEINFO
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _ATTRIBUTEINFO enumeration


## -description


The values of the 
<b>ATTRIBUTEINFO</b> type enumerate characteristics of a specified attribute.


## -enum-fields




### -field NAME

The name of the attribute.


### -field SYNTAX

The 
<a href="https://msdn.microsoft.com/50d56c43-6552-4bb0-a204-a0cfc3ee7202">syntax</a> of the attribute.


### -field RESTRICTIONS


<a href="https://msdn.microsoft.com/7a835536-3f5e-4c71-898c-e49d2f2da8ee">Restrictions</a> on how the attribute can be used.


### -field DESCRIPTION

Description of the attribute.


### -field VENDORID

The vendor ID for Vendor Specific Attributes (VSA).


### -field LDAPNAME

The Lightweight Directory Access Protocol (LDAP) name for the attribute.


### -field VENDORTYPE

The attribute type for Vendor Specific Attributes (VSA).


## -see-also




<a href="https://msdn.microsoft.com/7a835536-3f5e-4c71-898c-e49d2f2da8ee">ATTRIBUTERESTRICTIONS</a>



<a href="https://msdn.microsoft.com/50d56c43-6552-4bb0-a204-a0cfc3ee7202">ATTRIBUTESYNTAX</a>



<a href="https://msdn.microsoft.com/80535d3c-17bb-482b-b5bb-7d747f238b62">ISdoDictionaryOld::GetAttributeInfo</a>
 

 

