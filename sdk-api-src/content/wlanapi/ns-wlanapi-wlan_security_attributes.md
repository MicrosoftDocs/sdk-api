---
UID: NS:wlanapi._WLAN_SECURITY_ATTRIBUTES
title: WLAN_SECURITY_ATTRIBUTES (wlanapi.h)
author: windows-sdk-content
description: Defines the security attributes for a wireless connection.
old-location: nwifi\wlan_security_attributes.htm
tech.root: NativeWiFi
ms.assetid: 37aa07a2-fe7f-46e3-9f17-545f48442f35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES structure pointer [NativeWIFI], WLAN_SECURITY_ATTRIBUTES, WLAN_SECURITY_ATTRIBUTES structure [NativeWIFI], nwifi.wlan_security_attributes, wlanapi/PWLAN_SECURITY_ATTRIBUTES, wlanapi/WLAN_SECURITY_ATTRIBUTES"
ms.topic: struct
f1_keywords: 
 - "wlanapi/WLAN_SECURITY_ATTRIBUTES"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_SECURITY_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: WLAN_SECURITY_ATTRIBUTES, *PWLAN_SECURITY_ATTRIBUTES
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
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

A <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/dot11-auth-algorithm">DOT11_AUTH_ALGORITHM</a> value that identifies the authentication algorithm.


### -field dot11CipherAlgorithm

A <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/dot11-cipher-algorithm">DOT11_CIPHER_ALGORITHM</a> value that identifies the cipher algorithm.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/ns-wlanapi-_wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>
 

 

