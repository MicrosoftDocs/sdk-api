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

# _WLAN_POWER_SETTING enumeration


## -description


The <b>WLAN_POWER_SETTING</b> enumerated type specifies the power setting of an interface.


## -enum-fields




### -field wlan_power_setting_no_saving

Specifies no power-saving activity performed by the 802.11 station. 



### -field wlan_power_setting_low_saving

Specifies a power save polling (PSP) mode that uses the fastest power-saving mode. This power mode must provide the best combination of network performance and power usage. 



### -field wlan_power_setting_medium_saving

Specifies a PSP mode that uses the maximum (MAX) power saving capabilities. The MAX power save mode results in the greatest power savings for the radio on the 802.11 station. 



### -field wlan_power_setting_maximum_saving

Specifies a proprietary PSP mode implemented by the independent hardware vendor (IHV) that exceeds the wlan_power_setting_medium_saving power-saving level. 


### -field wlan_power_setting_invalid

The supplied power setting is invalid.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>
 

 

