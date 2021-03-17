---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
title: WLAN_HOSTED_NETWORK_SECURITY_SETTINGS (wlanapi.h)
description: Contains information about the security settings on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS","PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS","PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_SECURITY_SETTINGS","WLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure [NativeWIFI]","nwifi.wlan_hosted_network_security_settings","wlanapi/PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS","wlanapi/WLAN_HOSTED_NETWORK_SECURITY_SETTINGS"]
old-location: nwifi\wlan_hosted_network_security_settings.htm
tech.root: nwifi
ms.assetid: b86beb10-52e5-4bc0-95fe-08307f8d1ccd
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_SECURITY_SETTINGS, WLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure [NativeWIFI], nwifi.wlan_hosted_network_security_settings, wlanapi/PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, wlanapi/WLAN_HOSTED_NETWORK_SECURITY_SETTINGS'
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WLAN_HOSTED_NETWORK_SECURITY_SETTINGS, *PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
 - wlanapi/_WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
 - PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS
 - wlanapi/PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS
 - WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
 - wlanapi/WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
---

# WLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure


## -description

The <b>WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</b> structure contains information about the security settings on the wireless Hosted Network.

## -struct-fields

### -field dot11AuthAlgo

The authentication algorithm used by the wireless Hosted Network.

### -field dot11CipherAlgo

The cipher algorithm used by the wireless Hosted Network.

## -remarks

The <b>WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</b>  structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.

## -see-also

<a href="/windows/desktop/NativeWiFi/dot11-auth-algorithm">DOT11_AUTH_ALGORITHM</a>



<a href="/windows/desktop/NativeWiFi/dot11-cipher-algorithm">DOT11_CIPHER_ALGORITHM</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>