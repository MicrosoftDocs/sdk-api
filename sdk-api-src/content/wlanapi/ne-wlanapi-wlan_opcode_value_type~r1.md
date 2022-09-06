---
UID: NE:wlanapi._WLAN_OPCODE_VALUE_TYPE~r1
title: WLAN_OPCODE_VALUE_TYPE
ms.date: 01/30/2019
ms.keywords: _WLAN_OPCODE_VALUE_TYPE, WLAN_OPCODE_VALUE_TYPE
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
 - _WLAN_OPCODE_VALUE_TYPE
 - wlanapi/_WLAN_OPCODE_VALUE_TYPE
 - PWLAN_OPCODE_VALUE_TYPE
 - wlanapi/PWLAN_OPCODE_VALUE_TYPE
 - WLAN_OPCODE_VALUE_TYPE
 - wlanapi/WLAN_OPCODE_VALUE_TYPE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_OPCODE_VALUE_TYPE
 - WLAN_OPCODE_VALUE_TYPE
---

# WLAN_OPCODE_VALUE_TYPE enumeration


## -description

The <b>WLAN_OPCODE_VALUE_TYPE</b> enumeration specifies the origin of automatic configuration (auto config) settings.

## -enum-fields

### -field wlan_opcode_value_type_query_only:0

The auto config settings were queried, but the origin of the settings was not determined.

### -field wlan_opcode_value_type_set_by_group_policy

The auto config settings were set by group policy.

### -field wlan_opcode_value_type_set_by_user

The auto config settings were set by the user.

### -field wlan_opcode_value_type_invalid

The auto config settings are invalid.

## -remarks

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a>
