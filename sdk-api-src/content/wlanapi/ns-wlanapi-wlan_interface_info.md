---
UID: NS:wlanapi._WLAN_INTERFACE_INFO
title: WLAN_INTERFACE_INFO (wlanapi.h)
description: Contains information about a wireless LAN interface.
helpviewer_keywords: ["*PWLAN_INTERFACE_INFO","PWLAN_INTERFACE_INFO","PWLAN_INTERFACE_INFO structure pointer [NativeWIFI]","WLAN_INTERFACE_INFO","WLAN_INTERFACE_INFO structure [NativeWIFI]","nwifi.wlan_interface_info","wlanapi/PWLAN_INTERFACE_INFO","wlanapi/WLAN_INTERFACE_INFO"]
old-location: nwifi\wlan_interface_info.htm
tech.root: nwifi
ms.assetid: 906e7d59-ebd0-47e7-985e-f5d313f19ecb
ms.date: 12/05/2018
ms.keywords: '*PWLAN_INTERFACE_INFO, PWLAN_INTERFACE_INFO, PWLAN_INTERFACE_INFO structure pointer [NativeWIFI], WLAN_INTERFACE_INFO, WLAN_INTERFACE_INFO structure [NativeWIFI], nwifi.wlan_interface_info, wlanapi/PWLAN_INTERFACE_INFO, wlanapi/WLAN_INTERFACE_INFO'
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
req.typenames: WLAN_INTERFACE_INFO, *PWLAN_INTERFACE_INFO
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_INTERFACE_INFO
 - wlanapi/_WLAN_INTERFACE_INFO
 - PWLAN_INTERFACE_INFO
 - wlanapi/PWLAN_INTERFACE_INFO
 - WLAN_INTERFACE_INFO
 - wlanapi/WLAN_INTERFACE_INFO
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
 - WLAN_INTERFACE_INFO
---

# WLAN_INTERFACE_INFO structure


## -description

The <b>WLAN_INTERFACE_INFO</b> structure contains information about a wireless LAN interface.

## -struct-fields

### -field InterfaceGuid

Contains the GUID of the interface.

### -field strInterfaceDescription

Contains the description of the interface.

### -field isState

Contains a <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_interface_state-r1">WLAN_INTERFACE_STATE</a> value that indicates the current state of the interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_info_list">WLAN_INTERFACE_INFO_LIST</a>