---
UID: NE:wlanapi._WLAN_AUTOCONF_OPCODE~r1
title: WLAN_AUTOCONF_OPCODE
ms.date: 01/30/2019
ms.keywords: _WLAN_AUTOCONF_OPCODE, WLAN_AUTOCONF_OPCODE
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wlanapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - _WLAN_AUTOCONF_OPCODE
 - wlanapi/_WLAN_AUTOCONF_OPCODE
 - PWLAN_AUTOCONF_OPCODE
 - wlanapi/PWLAN_AUTOCONF_OPCODE
 - WLAN_AUTOCONF_OPCODE
 - wlanapi/WLAN_AUTOCONF_OPCODE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_AUTOCONF_OPCODE
 - WLAN_AUTOCONF_OPCODE
---

# WLAN_AUTOCONF_OPCODE enumeration


## -description

The <b>WLAN_AUTOCONF_OPCODE</b> enumerated type specifies an  automatic configuration parameter.

## -enum-fields

### -field wlan_autoconf_opcode_start:0

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

## -remarks

The <b>WLAN_AUTOCONF_OPCODE</b> enumerated type is used by the Auto Configuration Module (ACM), the wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_AUTOCONF_OPCODE</b> specifies the possible values for the <i>OpCode</i> parameter passed to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a> and <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetautoconfigparameter">WlanSetAutoConfigParameter</a> functions.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetautoconfigparameter">WlanSetAutoConfigParameter</a>
