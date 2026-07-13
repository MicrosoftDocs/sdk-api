---
UID: NE:wlanapi._WLAN_CONNECTION_MODE
title: WLAN_CONNECTION_MODE (wlanapi.h)
description: Defines the mode of connection.
helpviewer_keywords: ["*PWLAN_CONNECTION_MODE","PWLAN_CONNECTION_MODE","PWLAN_CONNECTION_MODE enumeration pointer [NativeWIFI]","WLAN_CONNECTION_MODE","WLAN_CONNECTION_MODE enumeration [NativeWIFI]","nwifi.wlan_connection_mode","wlan_connection_mode_auto","wlan_connection_mode_discovery_secure","wlan_connection_mode_discovery_unsecure","wlan_connection_mode_invalid","wlan_connection_mode_profile","wlan_connection_mode_temporary_profile","wlanapi/PWLAN_CONNECTION_MODE","wlanapi/WLAN_CONNECTION_MODE","wlanapi/wlan_connection_mode_auto","wlanapi/wlan_connection_mode_discovery_secure","wlanapi/wlan_connection_mode_discovery_unsecure","wlanapi/wlan_connection_mode_invalid","wlanapi/wlan_connection_mode_profile","wlanapi/wlan_connection_mode_temporary_profile"]
old-location: nwifi\wlan_connection_mode.htm
tech.root: nwifi
ms.assetid: d62e863f-2aa8-49b1-9e27-8d9d053026f0
ms.date: 12/05/2018
ms.keywords: '*PWLAN_CONNECTION_MODE, PWLAN_CONNECTION_MODE, PWLAN_CONNECTION_MODE enumeration pointer [NativeWIFI], WLAN_CONNECTION_MODE, WLAN_CONNECTION_MODE enumeration [NativeWIFI], nwifi.wlan_connection_mode, wlan_connection_mode_auto, wlan_connection_mode_discovery_secure, wlan_connection_mode_discovery_unsecure, wlan_connection_mode_invalid, wlan_connection_mode_profile, wlan_connection_mode_temporary_profile, wlanapi/PWLAN_CONNECTION_MODE, wlanapi/WLAN_CONNECTION_MODE, wlanapi/wlan_connection_mode_auto, wlanapi/wlan_connection_mode_discovery_secure, wlanapi/wlan_connection_mode_discovery_unsecure, wlanapi/wlan_connection_mode_invalid, wlanapi/wlan_connection_mode_profile, wlanapi/wlan_connection_mode_temporary_profile'
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
targetos: Windows
req.typenames: WLAN_CONNECTION_MODE, *PWLAN_CONNECTION_MODE
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_CONNECTION_MODE
 - wlanapi/_WLAN_CONNECTION_MODE
 - PWLAN_CONNECTION_MODE
 - wlanapi/PWLAN_CONNECTION_MODE
 - WLAN_CONNECTION_MODE
 - wlanapi/WLAN_CONNECTION_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_CONNECTION_MODE
---

# WLAN_CONNECTION_MODE enumeration


## -description

The <b>WLAN_CONNECTION_MODE</b> enumerated type defines the mode of connection.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.

## -enum-fields

### -field wlan_connection_mode_profile:0

A profile will be used to make the connection.

### -field wlan_connection_mode_temporary_profile

A temporary profile will be used to make the connection.

### -field wlan_connection_mode_discovery_secure

Secure discovery will be used to make the connection.

### -field wlan_connection_mode_discovery_unsecure

Unsecure discovery will be used to make the connection.

### -field wlan_connection_mode_auto

The connection is initiated by the wireless service automatically using a persistent profile.

### -field wlan_connection_mode_invalid

Not used.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a>
