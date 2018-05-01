---
UID: NE:wlanapi._WLAN_AUTOCONF_OPCODE
title: "_WLAN_AUTOCONF_OPCODE"
author: windows-driver-content
description: Specifies an automatic configuration parameter.
old-location: nwifi\wlan_autoconf_opcode.htm
old-project: NativeWiFi
ms.assetid: d7816d6f-0f8c-4d53-aa70-357aaca360d0
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PWLAN_AUTOCONF_OPCODE, PWLAN_AUTOCONF_OPCODE, PWLAN_AUTOCONF_OPCODE enumeration pointer [NativeWIFI], WLAN_AUTOCONF_OPCODE, WLAN_AUTOCONF_OPCODE enumeration [NativeWIFI], _WLAN_AUTOCONF_OPCODE, nwifi.wlan_autoconf_opcode, wlan_autoconf_opcode_allow_explicit_creds, wlan_autoconf_opcode_allow_virtual_station_extensibility, wlan_autoconf_opcode_block_period, wlan_autoconf_opcode_end, wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks, wlan_autoconf_opcode_power_setting, wlan_autoconf_opcode_show_denied_networks, wlan_autoconf_opcode_start, wlanapi/PWLAN_AUTOCONF_OPCODE, wlanapi/WLAN_AUTOCONF_OPCODE, wlanapi/wlan_autoconf_opcode_allow_explicit_creds, wlanapi/wlan_autoconf_opcode_allow_virtual_station_extensibility, wlanapi/wlan_autoconf_opcode_block_period, wlanapi/wlan_autoconf_opcode_end, wlanapi/wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks, wlanapi/wlan_autoconf_opcode_power_setting, wlanapi/wlan_autoconf_opcode_show_denied_networks, wlanapi/wlan_autoconf_opcode_start"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: WLAN_AUTOCONF_OPCODE, *PWLAN_AUTOCONF_OPCODE, WLAN_AUTOCONF_OPCODE, *PWLAN_AUTOCONF_OPCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_AUTOCONF_OPCODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_AUTOCONF_OPCODE enumeration


## -description


The <b>WLAN_AUTOCONF_OPCODE</b> enumerated type specifies an  automatic configuration parameter.


## -enum-fields




### -field wlan_autoconf_opcode_start

Not used.


### -field wlan_autoconf_opcode_show_denied_networks

The opcode used to set or query the parameter specifying  whether user and group policy denied networks will be included in the available networks list.


### -field wlan_autoconf_opcode_power_setting

The opcode used  to query the power settings.


### -field wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks

The opcode used to query whether profiles not created by group policy can be used to connect to an allowed network with a matching group policy profile.


### -field wlan_autoconf_opcode_allow_explicit_creds

The opcode used to set or query whether the current wireless interface has shared user credentials allowed.


### -field wlan_autoconf_opcode_block_period

The opcode used to set or query the blocked period setting for the current wireless interface. The blocked period is the amount of time, in seconds, for which automatic connection to a wireless network will not be attempted after a previous failure.


### -field wlan_autoconf_opcode_allow_virtual_station_extensibility

The opcode used to set or query whether extensibility on a virtual station is allowed. By default, extensibility on a virtual station is allowed. The value for this opcode is persisted across reboots.

This enumeration value is supported on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.


### -field wlan_autoconf_opcode_end

Not used.


### -field v1_enum




## -remarks



The <b>WLAN_AUTOCONF_OPCODE</b> enumerated type is used by the Auto Configuration Module (ACM), the wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_AUTOCONF_OPCODE</b> specifies the possible values for the <i>OpCode</i> parameter passed to the <a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a> and <a href="https://msdn.microsoft.com/4f2514be-f05e-4be6-8c74-ef7a9ffe1c53">WlanSetAutoConfigParameter</a> functions. 




## -see-also




<a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a>



<a href="https://msdn.microsoft.com/4f2514be-f05e-4be6-8c74-ef7a9ffe1c53">WlanSetAutoConfigParameter</a>
 

 

