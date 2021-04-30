---
UID: NS:wlanapi._WLAN_MSM_NOTIFICATION_DATA
title: WLAN_MSM_NOTIFICATION_DATA (wlanapi.h)
description: Contains information about media specific module (MSM) connection related notifications.
helpviewer_keywords: ["*PWLAN_MSM_NOTIFICATION_DATA","PWLAN_MSM_NOTIFICATION_DATA","PWLAN_MSM_NOTIFICATION_DATA structure pointer [NativeWIFI]","WLAN_MSM_NOTIFICATION_DATA","WLAN_MSM_NOTIFICATION_DATA structure [NativeWIFI]","nwifi.wlan_msm_notification_data","wlanapi/PWLAN_MSM_NOTIFICATION_DATA","wlanapi/WLAN_MSM_NOTIFICATION_DATA"]
old-location: nwifi\wlan_msm_notification_data.htm
tech.root: nwifi
ms.assetid: 76693a8e-7df8-45f0-a3c1-7960de27250c
ms.date: 12/05/2018
ms.keywords: '*PWLAN_MSM_NOTIFICATION_DATA, PWLAN_MSM_NOTIFICATION_DATA, PWLAN_MSM_NOTIFICATION_DATA structure pointer [NativeWIFI], WLAN_MSM_NOTIFICATION_DATA, WLAN_MSM_NOTIFICATION_DATA structure [NativeWIFI], nwifi.wlan_msm_notification_data, wlanapi/PWLAN_MSM_NOTIFICATION_DATA, wlanapi/WLAN_MSM_NOTIFICATION_DATA'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: WLAN_MSM_NOTIFICATION_DATA, *PWLAN_MSM_NOTIFICATION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_MSM_NOTIFICATION_DATA
 - wlanapi/_WLAN_MSM_NOTIFICATION_DATA
 - PWLAN_MSM_NOTIFICATION_DATA
 - wlanapi/PWLAN_MSM_NOTIFICATION_DATA
 - WLAN_MSM_NOTIFICATION_DATA
 - wlanapi/WLAN_MSM_NOTIFICATION_DATA
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
 - WLAN_MSM_NOTIFICATION_DATA
---

# WLAN_MSM_NOTIFICATION_DATA structure


## -description

The <b>WLAN_MSM_NOTIFICATION_DATA</b> structure contains information about media specific module (MSM) connection related notifications.

## -struct-fields

### -field wlanConnectionMode

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_connection_mode">WLAN_CONNECTION_MODE</a> value that specifies the mode of the connection.

### -field strProfileName

The name of the profile used for the connection. WLAN_MAX_NAME_LENGTH is 256. Profile names are case-sensitive. This string must be NULL-terminated.

### -field dot11Ssid

A <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that contains the SSID of the association.

### -field dot11BssType

A <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> value that indicates the BSS network type.

### -field dot11MacAddr

A <a href="/windows/desktop/NativeWiFi/dot11-mac-address-type">DOT11_MAC_ADDRESS</a> that specifies the MAC address of the peer or access point.

### -field bSecurityEnabled

Indicates whether security is enabled for this connection.  If <b>TRUE</b>, security is enabled.

### -field bFirstPeer

Indicates whether the peer is the first to join the ad hoc network created by the machine. If <b>TRUE</b>, the peer is the first to join.

After the first peer joins the network, the interface state of the machine that created the ad hoc network changes from wlan_interface_state_ad_hoc_network_formed to wlan_interface_state_connected.

### -field bLastPeer

Indicates whether the peer is the last to leave the ad hoc network created by the machine. If <b>TRUE</b>, the peer is the last to leave. After the last peer leaves the network, the interface state of the machine that created the ad hoc network changes from wlan_interface_state_connected to wlan_interface_state_ad_hoc_network_formed.

### -field wlanReasonCode

A <a href="/windows/desktop/NativeWiFi/wlan-reason-code">WLAN_REASON_CODE</a> that indicates the reason for an operation failure.  If the operation succeeds, this field has a value of <b>WLAN_REASON_CODE_SUCCESS</b>. Otherwise, this field indicates the reason for the failure.

## -remarks

The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. 

If the <b>NotificationSource</b> member of the  <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure received by the callback function is <b>WLAN_NOTIFICATION_SOURCE_MSM</b>, then the received notification is a media specific module (MSM) notification. The <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure passed to the <a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a> function  determines the interpretation of the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure.  For some of these notifications, a <b>WLAN_MSM_NOTIFICATION_DATA</b> structure is returned in the <i>pData</i> member of <b>WLAN_NOTIFICATION_DATA</b> structure. 

For more information on these notifications, see the <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_notification_msm-r1">WLAN_NOTIFICATION_MSM</a> enumeration reference.

## -see-also

<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_notification_msm-r1">WLAN_NOTIFICATION_MSM</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>