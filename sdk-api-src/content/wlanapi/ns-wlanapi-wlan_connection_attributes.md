---
UID: NS:wlanapi._WLAN_CONNECTION_ATTRIBUTES
title: WLAN_CONNECTION_ATTRIBUTES (wlanapi.h)
description: Defines the attributes of a wireless connection.
helpviewer_keywords: ["*PWLAN_CONNECTION_ATTRIBUTES","PWLAN_CONNECTION_ATTRIBUTES","PWLAN_CONNECTION_ATTRIBUTES structure pointer [NativeWIFI]","WLAN_CONNECTION_ATTRIBUTES","WLAN_CONNECTION_ATTRIBUTES structure [NativeWIFI]","nwifi.wlan_connection_attributes","wlanapi/PWLAN_CONNECTION_ATTRIBUTES","wlanapi/WLAN_CONNECTION_ATTRIBUTES"]
old-location: nwifi\wlan_connection_attributes.htm
tech.root: nwifi
ms.assetid: 91b8058d-faf6-46ee-a03b-f762e9cdae4d
ms.date: 12/05/2018
ms.keywords: '*PWLAN_CONNECTION_ATTRIBUTES, PWLAN_CONNECTION_ATTRIBUTES, PWLAN_CONNECTION_ATTRIBUTES structure pointer [NativeWIFI], WLAN_CONNECTION_ATTRIBUTES, WLAN_CONNECTION_ATTRIBUTES structure [NativeWIFI], nwifi.wlan_connection_attributes, wlanapi/PWLAN_CONNECTION_ATTRIBUTES, wlanapi/WLAN_CONNECTION_ATTRIBUTES'
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
req.typenames: WLAN_CONNECTION_ATTRIBUTES, *PWLAN_CONNECTION_ATTRIBUTES
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_CONNECTION_ATTRIBUTES
 - wlanapi/_WLAN_CONNECTION_ATTRIBUTES
 - PWLAN_CONNECTION_ATTRIBUTES
 - wlanapi/PWLAN_CONNECTION_ATTRIBUTES
 - WLAN_CONNECTION_ATTRIBUTES
 - wlanapi/WLAN_CONNECTION_ATTRIBUTES
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
 - WLAN_CONNECTION_ATTRIBUTES
---

# WLAN_CONNECTION_ATTRIBUTES structure


## -description

The <b>WLAN_CONNECTION_ATTRIBUTES</b> structure defines the attributes of a wireless connection.

## -struct-fields

### -field isState

A <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_interface_state-r1">WLAN_INTERFACE_STATE</a> value that indicates the state of the interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.

### -field wlanConnectionMode

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_connection_mode">WLAN_CONNECTION_MODE</a> value that indicates the mode of the connection.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.

### -field strProfileName

The name of the profile used for the connection. Profile names are case-sensitive. This string must be NULL-terminated.

### -field wlanAssociationAttributes

A <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes">WLAN_ASSOCIATION_ATTRIBUTES</a> structure  that contains the attributes of the association.

### -field wlanSecurityAttributes

A <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes">WLAN_SECURITY_ATTRIBUTES</a> structure that contains the security attributes of the connection.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>