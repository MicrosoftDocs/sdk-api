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
 

 

