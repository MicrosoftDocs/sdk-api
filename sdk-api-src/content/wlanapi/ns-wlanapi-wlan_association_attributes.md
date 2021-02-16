---
UID: NS:wlanapi._WLAN_ASSOCIATION_ATTRIBUTES
title: WLAN_ASSOCIATION_ATTRIBUTES (wlanapi.h)
description: Contains association attributes for a connection.
helpviewer_keywords: ["*PWLAN_ASSOCIATION_ATTRIBUTES","PWLAN_ASSOCIATION_ATTRIBUTES","PWLAN_ASSOCIATION_ATTRIBUTES structure pointer [NativeWIFI]","WLAN_ASSOCIATION_ATTRIBUTES","WLAN_ASSOCIATION_ATTRIBUTES structure [NativeWIFI]","nwifi.wlan_association_attributes","wlanapi/PWLAN_ASSOCIATION_ATTRIBUTES","wlanapi/WLAN_ASSOCIATION_ATTRIBUTES"]
old-location: nwifi\wlan_association_attributes.htm
tech.root: nwifi
ms.assetid: f7d3d106-54a9-4bdf-bccf-216cac938995
ms.date: 12/05/2018
ms.keywords: '*PWLAN_ASSOCIATION_ATTRIBUTES, PWLAN_ASSOCIATION_ATTRIBUTES, PWLAN_ASSOCIATION_ATTRIBUTES structure pointer [NativeWIFI], WLAN_ASSOCIATION_ATTRIBUTES, WLAN_ASSOCIATION_ATTRIBUTES structure [NativeWIFI], nwifi.wlan_association_attributes, wlanapi/PWLAN_ASSOCIATION_ATTRIBUTES, wlanapi/WLAN_ASSOCIATION_ATTRIBUTES'
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
req.typenames: WLAN_ASSOCIATION_ATTRIBUTES, *PWLAN_ASSOCIATION_ATTRIBUTES
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_ASSOCIATION_ATTRIBUTES
 - wlanapi/_WLAN_ASSOCIATION_ATTRIBUTES
 - PWLAN_ASSOCIATION_ATTRIBUTES
 - wlanapi/PWLAN_ASSOCIATION_ATTRIBUTES
 - WLAN_ASSOCIATION_ATTRIBUTES
 - wlanapi/WLAN_ASSOCIATION_ATTRIBUTES
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
 - WLAN_ASSOCIATION_ATTRIBUTES
---

# WLAN_ASSOCIATION_ATTRIBUTES structure


## -description

The <b>WLAN_ASSOCIATION_ATTRIBUTES</b> structure contains association attributes for a connection.

## -struct-fields

### -field dot11Ssid

A <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that contains the SSID of the association.

### -field dot11BssType

A <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> value that specifies whether the network is infrastructure or ad hoc.

### -field dot11Bssid

A <a href="/windows/desktop/NativeWiFi/dot11-mac-address-type">DOT11_MAC_ADDRESS</a> that contains the BSSID of the association.

### -field dot11PhyType

A <a href="/windows/desktop/NativeWiFi/dot11-phy-type">DOT11_PHY_TYPE</a> value that indicates the physical type of the association.

### -field uDot11PhyIndex

The position of the <a href="/windows/desktop/NativeWiFi/dot11-phy-type">DOT11_PHY_TYPE</a> value in the structure containing the list of PHY types.

### -field wlanSignalQuality

A percentage value that represents the signal quality of the network.  <b>WLAN_SIGNAL_QUALITY</b> is of type <b>ULONG</b>.  This member contains a value between 0 and 100. A value of 0 implies an actual RSSI signal strength of -100 dbm. A value of 100 implies an actual RSSI signal strength of -50 dbm. You can calculate the RSSI signal strength value for <b>wlanSignalQuality</b> values between 1 and 99 using linear interpolation.

### -field ulRxRate

Contains the receiving rate of the association.

### -field ulTxRate

Contains the transmission rate of the association.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>