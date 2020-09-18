---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_OPCODE
title: WLAN_HOSTED_NETWORK_OPCODE (wlanapi.h)
description: Specifies the possible values of the operation code for the properties to query or set on the wireless Hosted Network.
helpviewer_keywords: ["*PWLAN_HOSTED_NETWORK_OPCODE","PWLAN_HOSTED_NETWORK_OPCODE","PWLAN_HOSTED_NETWORK_OPCODE enumeration pointer [NativeWIFI]","WLAN_HOSTED_NETWORK_OPCODE","WLAN_HOSTED_NETWORK_OPCODE enumeration [NativeWIFI]","nwifi.wlan_hosted_network_opcode","wlan_hosted_network_opcode_connection_settings","wlan_hosted_network_opcode_enable","wlan_hosted_network_opcode_security_settings","wlan_hosted_network_opcode_station_profile","wlanapi/PWLAN_HOSTED_NETWORK_OPCODE","wlanapi/WLAN_HOSTED_NETWORK_OPCODE","wlanapi/wlan_hosted_network_opcode_connection_settings","wlanapi/wlan_hosted_network_opcode_enable","wlanapi/wlan_hosted_network_opcode_security_settings","wlanapi/wlan_hosted_network_opcode_station_profile"]
old-location: nwifi\wlan_hosted_network_opcode.htm
tech.root: nwifi
ms.assetid: e4acd7ad-c8f2-4ece-8d27-ced879baa9e7
ms.date: 12/05/2018
ms.keywords: '*PWLAN_HOSTED_NETWORK_OPCODE, PWLAN_HOSTED_NETWORK_OPCODE, PWLAN_HOSTED_NETWORK_OPCODE enumeration pointer [NativeWIFI], WLAN_HOSTED_NETWORK_OPCODE, WLAN_HOSTED_NETWORK_OPCODE enumeration [NativeWIFI], nwifi.wlan_hosted_network_opcode, wlan_hosted_network_opcode_connection_settings, wlan_hosted_network_opcode_enable, wlan_hosted_network_opcode_security_settings, wlan_hosted_network_opcode_station_profile, wlanapi/PWLAN_HOSTED_NETWORK_OPCODE, wlanapi/WLAN_HOSTED_NETWORK_OPCODE, wlanapi/wlan_hosted_network_opcode_connection_settings, wlanapi/wlan_hosted_network_opcode_enable, wlanapi/wlan_hosted_network_opcode_security_settings, wlanapi/wlan_hosted_network_opcode_station_profile'
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
req.typenames: WLAN_HOSTED_NETWORK_OPCODE, *PWLAN_HOSTED_NETWORK_OPCODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_HOSTED_NETWORK_OPCODE
 - wlanapi/_WLAN_HOSTED_NETWORK_OPCODE
 - PWLAN_HOSTED_NETWORK_OPCODE
 - wlanapi/PWLAN_HOSTED_NETWORK_OPCODE
 - WLAN_HOSTED_NETWORK_OPCODE
 - wlanapi/WLAN_HOSTED_NETWORK_OPCODE
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
 - WLAN_HOSTED_NETWORK_OPCODE
---

# WLAN_HOSTED_NETWORK_OPCODE enumeration


## -description

The <b>WLAN_HOSTED_NETWORK_OPCODE</b> enumerated type specifies the possible values of the operation code for the properties to query or set on the wireless Hosted Network.

## -enum-fields

### -field wlan_hosted_network_opcode_connection_settings

The opcode used to query or set the wireless Hosted Network connection settings.

### -field wlan_hosted_network_opcode_security_settings

The opcode used to query the wireless Hosted Network security settings.

### -field wlan_hosted_network_opcode_station_profile

The opcode used to query the wireless Hosted Network station profile.

### -field wlan_hosted_network_opcode_enable

The opcode used to query or set the wireless Hosted Network enabled flag.

### -field v1_enum

## -remarks

The <b>WLAN_HOSTED_NETWORK_OPCODE</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  

The <b>WLAN_HOSTED_NETWORK_OPCODE</b> specifies the possible values of the operation code for the properties to query or set on the wireless Hosted Network.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>