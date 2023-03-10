---
UID: NE:wlanapi._WLAN_INTERFACE_STATE~r1
title: WLAN_INTERFACE_STATE
description: The WLAN_INTERFACE_STATE enumeration indicates the state of an interface.
ms.date: 08/16/2022
ms.keywords: _WLAN_INTERFACE_STATE, WLAN_INTERFACE_STATE
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
 - _WLAN_INTERFACE_STATE
 - wlanapi/_WLAN_INTERFACE_STATE
 - PWLAN_INTERFACE_STATE
 - wlanapi/PWLAN_INTERFACE_STATE
 - WLAN_INTERFACE_STATE
 - wlanapi/WLAN_INTERFACE_STATE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_INTERFACE_STATE
 - WLAN_INTERFACE_STATE
---

# WLAN_INTERFACE_STATE enumeration


## -description

The <b>WLAN_INTERFACE_STATE</b> enumerated type indicates the state of an interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.

## -enum-fields

### -field wlan_interface_state_not_ready

The interface is not ready to operate.

### -field wlan_interface_state_connected

The interface is connected to a network.

### -field wlan_interface_state_ad_hoc_network_formed

The interface is the first node in an ad hoc network.  No peer has connected.

### -field wlan_interface_state_disconnecting

The interface is disconnecting from the current network.

### -field wlan_interface_state_disconnected

The interface is not connected to any network.

### -field wlan_interface_state_associating

The interface is attempting to associate with a network.

### -field wlan_interface_state_discovering

Auto configuration is discovering the settings for the network.

### -field wlan_interface_state_authenticating

The interface is in the process of authenticating.

## -remarks

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_info">WLAN_INTERFACE_INFO</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>
