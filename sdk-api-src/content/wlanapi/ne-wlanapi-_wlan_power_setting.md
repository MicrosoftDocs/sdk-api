---
UID: NE:wlanapi._WLAN_POWER_SETTING
title: "_WLAN_POWER_SETTING"
author: windows-sdk-content
description: Specifies the power setting of an interface.
old-location: nwifi\wlan_power_setting.htm
tech.root: NativeWiFi
ms.assetid: f2509c87-8a2a-4e6e-9995-e824a17e7083
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWLAN_POWER_SETTING, PWLAN_POWER_SETTING, PWLAN_POWER_SETTING enumeration pointer [NativeWIFI], WLAN_POWER_SETTING, WLAN_POWER_SETTING enumeration [NativeWIFI], _WLAN_POWER_SETTING, nwifi.wlan_power_setting, wlan_power_setting_invalid, wlan_power_setting_low_saving, wlan_power_setting_maximum_saving, wlan_power_setting_medium_saving, wlan_power_setting_no_saving, wlanapi/PWLAN_POWER_SETTING, wlanapi/WLAN_POWER_SETTING, wlanapi/wlan_power_setting_invalid, wlanapi/wlan_power_setting_low_saving, wlanapi/wlan_power_setting_maximum_saving, wlanapi/wlan_power_setting_medium_saving, wlanapi/wlan_power_setting_no_saving"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - wlanapi.h
api_name:
 - WLAN_POWER_SETTING
product: Windows
targetos: Windows
req.typenames: WLAN_POWER_SETTING, *PWLAN_POWER_SETTING
req.redist: Wireless LAN API for Windows XP with SP2
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
 

 

