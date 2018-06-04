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

# _WLAN_HOSTED_NETWORK_OPCODE enumeration


## -description


The <b>WLAN_HOSTED_NETWORK_OPCODE</b> enumerated type specifies the possible values of the operation code for the properties to query or set on the wireless Hosted Network.


## -enum-fields




### -field wlan_hosted_network_opcode_connection_settings

The opcode used to query or set the wireless Hosted Network connection settings.


### -field wlan_hosted_network_opcode_security_settings

The opcode used to query the wireless Hosted Network security settings.


### -field wlan_hosted_network_opcode_station_profile

The opcode used to query the wireless Hosted Network station profile.


### -field wlan_hosted_network_opcode_enable

The opcode used to query or set the wireless Hosted Network enabled flag.


### -field v1_enum




## -remarks



The <b>WLAN_HOSTED_NETWORK_OPCODE</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  

The <b>WLAN_HOSTED_NETWORK_OPCODE</b> specifies the possible values of the operation code for the properties to query or set on the wireless Hosted Network. 




## -see-also




<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a>
 

 

