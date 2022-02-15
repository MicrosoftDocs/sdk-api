---
UID: NE:wlanapi._WLAN_POWER_SETTING~r1
title: WLAN_POWER_SETTING
ms.date: 01/30/2019
ms.keywords: _WLAN_POWER_SETTING, WLAN_POWER_SETTING
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
 - _WLAN_POWER_SETTING
 - wlanapi/_WLAN_POWER_SETTING
 - PWLAN_POWER_SETTING
 - wlanapi/PWLAN_POWER_SETTING
 - WLAN_POWER_SETTING
 - wlanapi/WLAN_POWER_SETTING
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_POWER_SETTING
 - WLAN_POWER_SETTING
---

# WLAN_POWER_SETTING enumeration


## -description

The <b>WLAN_POWER_SETTING</b> enumerated type specifies the power setting of an interface.

## -enum-fields

### -field wlan_power_setting_no_saving:0

Specifies no power-saving activity performed by the 802.11 station.

### -field wlan_power_setting_low_saving

Specifies a power save polling (PSP) mode that uses the fastest power-saving mode. This power mode must provide the best combination of network performance and power usage.

### -field wlan_power_setting_medium_saving

Specifies a PSP mode that uses the maximum (MAX) power saving capabilities. The MAX power save mode results in the greatest power savings for the radio on the 802.11 station.

### -field wlan_power_setting_maximum_saving

Specifies a proprietary PSP mode implemented by the independent hardware vendor (IHV) that exceeds the wlan_power_setting_medium_saving power-saving level.

### -field wlan_power_setting_invalid

The supplied power setting is invalid.

## -remarks

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>
