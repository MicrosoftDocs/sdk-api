---
UID: NS:wlanapi._WLAN_SECURITY_ATTRIBUTES
title: WLAN_SECURITY_ATTRIBUTES (wlanapi.h)
description: Defines the security attributes for a wireless connection.
helpviewer_keywords: ["*PWLAN_SECURITY_ATTRIBUTES","PWLAN_SECURITY_ATTRIBUTES","PWLAN_SECURITY_ATTRIBUTES structure pointer [NativeWIFI]","WLAN_SECURITY_ATTRIBUTES","WLAN_SECURITY_ATTRIBUTES structure [NativeWIFI]","nwifi.wlan_security_attributes","wlanapi/PWLAN_SECURITY_ATTRIBUTES","wlanapi/WLAN_SECURITY_ATTRIBUTES"]
old-location: nwifi\wlan_security_attributes.htm
tech.root: nwifi
ms.assetid: 37aa07a2-fe7f-46e3-9f17-545f48442f35
ms.date: 12/05/2018
ms.keywords: '*PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES structure pointer [NativeWIFI], WLAN_SECURITY_ATTRIBUTES, WLAN_SECURITY_ATTRIBUTES structure [NativeWIFI], nwifi.wlan_security_attributes, wlanapi/PWLAN_SECURITY_ATTRIBUTES, wlanapi/WLAN_SECURITY_ATTRIBUTES'
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
req.typenames: WLAN_SECURITY_ATTRIBUTES, *PWLAN_SECURITY_ATTRIBUTES
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_SECURITY_ATTRIBUTES
 - wlanapi/_WLAN_SECURITY_ATTRIBUTES
 - PWLAN_SECURITY_ATTRIBUTES
 - wlanapi/PWLAN_SECURITY_ATTRIBUTES
 - WLAN_SECURITY_ATTRIBUTES
 - wlanapi/WLAN_SECURITY_ATTRIBUTES
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
 - WLAN_SECURITY_ATTRIBUTES
---

# WLAN_SECURITY_ATTRIBUTES structure


## -description

The <b>WLAN_SECURITY_ATTRIBUTES</b> structure defines the security attributes for a wireless connection.

## -struct-fields

### -field bSecurityEnabled

Indicates whether security is enabled for this connection.

### -field bOneXEnabled

Indicates whether 802.1X is enabled for this connection.

### -field dot11AuthAlgorithm

A <a href="/windows/desktop/NativeWiFi/dot11-auth-algorithm">DOT11_AUTH_ALGORITHM</a> value that identifies the authentication algorithm.

### -field dot11CipherAlgorithm

A <a href="/windows/desktop/NativeWiFi/dot11-cipher-algorithm">DOT11_CIPHER_ALGORITHM</a> value that identifies the cipher algorithm.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>