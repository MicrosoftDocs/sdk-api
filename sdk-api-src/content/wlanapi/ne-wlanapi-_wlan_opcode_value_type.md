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

# _WLAN_OPCODE_VALUE_TYPE enumeration


## -description


The <b>WLAN_OPCODE_VALUE_TYPE</b> enumeration specifies the origin of automatic configuration (auto config) settings. 


## -enum-fields




### -field wlan_opcode_value_type_query_only

The auto config settings were queried, but the origin of the settings was not determined. 


### -field wlan_opcode_value_type_set_by_group_policy

The auto config settings were set by group policy.


### -field wlan_opcode_value_type_set_by_user

The auto config settings were set by the user.


### -field wlan_opcode_value_type_invalid

The auto config settings are invalid.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a>
 

 

