---
UID: NE:sdoias._ATTRIBUTERESTRICTIONS
title: "_ATTRIBUTERESTRICTIONS"
author: windows-sdk-content
description: The values of the ATTRIBUTERESTRICTIONS enumeration type specify restrictions on how a particular attribute can be used.
old-location: nps\SDO_attributerestrictions.htm
old-project: nps
ms.assetid: 7a835536-3f5e-4c71-898c-e49d2f2da8ee
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ALLOWEDIN8021X, ALLOWEDINCONDITION, ALLOWEDINPROFILE, ALLOWEDINPROXYCONDITION, ALLOWEDINPROXYPROFILE, ALLOWEDINVPNDIALUP, ATTRIBUTERESTRICTIONS, ATTRIBUTERESTRICTIONS enumeration [Network Policy Server], MULTIVALUED, _ATTRIBUTERESTRICTIONS, _sdo_attributerestrictions, nps.SDO_attributerestrictions, sdo.attributerestrictions, sdoias/ALLOWEDIN8021X, sdoias/ALLOWEDINCONDITION, sdoias/ALLOWEDINPROFILE, sdoias/ALLOWEDINPROXYCONDITION, sdoias/ALLOWEDINPROXYPROFILE, sdoias/ALLOWEDINVPNDIALUP, sdoias/ATTRIBUTERESTRICTIONS, sdoias/MULTIVALUED
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ATTRIBUTERESTRICTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - ATTRIBUTERESTRICTIONS
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# _ATTRIBUTERESTRICTIONS enumeration


## -description


The values of the 
<b>ATTRIBUTERESTRICTIONS</b> enumeration type specify restrictions on how a particular attribute can be used.


## -enum-fields




### -field MULTIVALUED

Specifies whether the attribute is multivalued.


### -field ALLOWEDINPROFILE

Specifies whether the attribute is allowed in a Network Access Policy (NAP) profile.


### -field ALLOWEDINCONDITION

Specifies whether the attribute is allowed in an NAP condition.


### -field ALLOWEDINPROXYPROFILE

Specifies whether the attribute is allowed in an NAP profile for a network request proxy.


### -field ALLOWEDINPROXYCONDITION

Specifies whether the attribute is allowed in an NAP condition for a network request proxy.


### -field ALLOWEDINVPNDIALUP

Specifies whether the attribute is allowed in a VPN dialup connection.


### -field ALLOWEDIN8021X

Specifies whether the attribute is allowed in an 8021x connection.


## -see-also




<a href="https://msdn.microsoft.com/84ed435c-c6e8-41e7-9a5f-acd78fce4a10">ATTRIBUTEINFO</a>
 

 

