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
 

 

