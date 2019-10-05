---
UID: NE:sdoias._ATTRIBUTEINFO
title: ATTRIBUTEINFO (sdoias.h)
author: windows-sdk-content
description: The values of the ATTRIBUTEINFO type enumerate characteristics of a specified attribute.
old-location: nps\SDO_attributeinfo.htm
tech.root: Nps
ms.assetid: 84ed435c-c6e8-41e7-9a5f-acd78fce4a10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ATTRIBUTEINFO, ATTRIBUTEINFO enumeration [Network Policy Server], DESCRIPTION, LDAPNAME, NAME, RESTRICTIONS, SYNTAX, VENDORID, VENDORTYPE, _sdo_attributeinfo, nps.SDO_attributeinfo, sdo.attributeinfo, sdoias/ATTRIBUTEINFO, sdoias/DESCRIPTION, sdoias/LDAPNAME, sdoias/NAME, sdoias/RESTRICTIONS, sdoias/SYNTAX, sdoias/VENDORID, sdoias/VENDORTYPE
ms.topic: enum
f1_keywords:
- sdoias/ATTRIBUTEINFO
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- SdoIas.h
api_name:
- ATTRIBUTEINFO
targetos: Windows
req.typenames: ATTRIBUTEINFO
req.redist: 
ms.custom: 19H1
---

# ATTRIBUTEINFO enumeration


## -description


The values of the 
<b>ATTRIBUTEINFO</b> type enumerate characteristics of a specified attribute.


## -enum-fields




### -field NAME

The name of the attribute.


### -field SYNTAX

The 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-attributesyntax">syntax</a> of the attribute.


### -field RESTRICTIONS


<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-attributerestrictions">Restrictions</a> on how the attribute can be used.


### -field DESCRIPTION

Description of the attribute.


### -field VENDORID

The vendor ID for Vendor Specific Attributes (VSA).


### -field LDAPNAME

The Lightweight Directory Access Protocol (LDAP) name for the attribute.


### -field VENDORTYPE

The attribute type for Vendor Specific Attributes (VSA).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-attributerestrictions">ATTRIBUTERESTRICTIONS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-attributesyntax">ATTRIBUTESYNTAX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdodictionaryold-getattributeinfo">ISdoDictionaryOld::GetAttributeInfo</a>
 

 

