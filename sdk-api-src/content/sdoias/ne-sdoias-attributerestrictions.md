---
UID: NE:sdoias._ATTRIBUTERESTRICTIONS
title: ATTRIBUTERESTRICTIONS (sdoias.h)
description: The values of the ATTRIBUTERESTRICTIONS enumeration type specify restrictions on how a particular attribute can be used.
helpviewer_keywords: ["ALLOWEDIN8021X","ALLOWEDINCONDITION","ALLOWEDINPROFILE","ALLOWEDINPROXYCONDITION","ALLOWEDINPROXYPROFILE","ALLOWEDINVPNDIALUP","ATTRIBUTERESTRICTIONS","ATTRIBUTERESTRICTIONS enumeration [Network Policy Server]","MULTIVALUED","_sdo_attributerestrictions","nps.SDO_attributerestrictions","sdo.attributerestrictions","sdoias/ALLOWEDIN8021X","sdoias/ALLOWEDINCONDITION","sdoias/ALLOWEDINPROFILE","sdoias/ALLOWEDINPROXYCONDITION","sdoias/ALLOWEDINPROXYPROFILE","sdoias/ALLOWEDINVPNDIALUP","sdoias/ATTRIBUTERESTRICTIONS","sdoias/MULTIVALUED"]
old-location: nps\SDO_attributerestrictions.htm
tech.root: Nps
ms.assetid: 7a835536-3f5e-4c71-898c-e49d2f2da8ee
ms.date: 12/05/2018
ms.keywords: ALLOWEDIN8021X, ALLOWEDINCONDITION, ALLOWEDINPROFILE, ALLOWEDINPROXYCONDITION, ALLOWEDINPROXYPROFILE, ALLOWEDINVPNDIALUP, ATTRIBUTERESTRICTIONS, ATTRIBUTERESTRICTIONS enumeration [Network Policy Server], MULTIVALUED, _sdo_attributerestrictions, nps.SDO_attributerestrictions, sdo.attributerestrictions, sdoias/ALLOWEDIN8021X, sdoias/ALLOWEDINCONDITION, sdoias/ALLOWEDINPROFILE, sdoias/ALLOWEDINPROXYCONDITION, sdoias/ALLOWEDINPROXYPROFILE, sdoias/ALLOWEDINVPNDIALUP, sdoias/ATTRIBUTERESTRICTIONS, sdoias/MULTIVALUED
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
req.typenames: ATTRIBUTERESTRICTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ATTRIBUTERESTRICTIONS
 - sdoias/_ATTRIBUTERESTRICTIONS
 - ATTRIBUTERESTRICTIONS
 - sdoias/ATTRIBUTERESTRICTIONS
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
 - ATTRIBUTERESTRICTIONS
---

# ATTRIBUTERESTRICTIONS enumeration


## -description

The values of the 
<b>ATTRIBUTERESTRICTIONS</b> enumeration type specify restrictions on how a particular attribute can be used.

## -enum-fields

### -field MULTIVALUED:0x1

Specifies whether the attribute is multivalued.

### -field ALLOWEDINPROFILE:0x2

Specifies whether the attribute is allowed in a Network Access Policy (NAP) profile.

### -field ALLOWEDINCONDITION:0x4

Specifies whether the attribute is allowed in an NAP condition.

### -field ALLOWEDINPROXYPROFILE:0x8

Specifies whether the attribute is allowed in an NAP profile for a network request proxy.

### -field ALLOWEDINPROXYCONDITION:0x10

Specifies whether the attribute is allowed in an NAP condition for a network request proxy.

### -field ALLOWEDINVPNDIALUP:0x20

Specifies whether the attribute is allowed in a VPN dialup connection.

### -field ALLOWEDIN8021X:0x40

Specifies whether the attribute is allowed in an 8021x connection.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-attributeinfo">ATTRIBUTEINFO</a>
