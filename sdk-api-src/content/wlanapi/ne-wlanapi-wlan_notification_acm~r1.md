---
UID: NE:wlanapi._WLAN_NOTIFICATION_ACM~r1
title: WLAN_NOTIFICATION_ACM
description: The WLAN_NOTIFICATION_ACM enumeration specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure.
ms.date: 08/16/2022
ms.keywords: _WLAN_NOTIFICATION_ACM, WLAN_NOTIFICATION_ACM
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
 - _WLAN_NOTIFICATION_ACM
 - wlanapi/_WLAN_NOTIFICATION_ACM
 - PWLAN_NOTIFICATION_ACM
 - wlanapi/PWLAN_NOTIFICATION_ACM
 - WLAN_NOTIFICATION_ACM
 - wlanapi/WLAN_NOTIFICATION_ACM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_NOTIFICATION_ACM
 - WLAN_NOTIFICATION_ACM
---

# WLAN_NOTIFICATION_ACM enumeration


## -description

The <b>WLAN_NOTIFICATION_ACM</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for Auto Configuration Module  (ACM) notifications.

## -enum-fields

### -field wlan_notification_acm_start

Indicates the beginning of the range that specifies the possible values for ACM notifications.

### -field wlan_notification_acm_autoconf_enabled

Autoconfiguration is enabled.

### -field wlan_notification_acm_autoconf_disabled

Autoconfiguration is disabled.

### -field wlan_notification_acm_background_scan_enabled

Background scans are enabled.

### -field wlan_notification_acm_background_scan_disabled

Background scans are disabled.

### -field wlan_notification_acm_bss_type_change

The BSS type for an interface has changed.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> enumeration value that identifies the new basic service set (BSS) type.

### -field wlan_notification_acm_power_setting_change

The power setting for an interface has changed.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_power_setting-r1">WLAN_POWER_SETTING</a> enumeration value that identifies the new power setting of an interface.

### -field wlan_notification_acm_scan_complete

A scan for networks has completed.

### -field wlan_notification_acm_scan_fail

A scan for connectable networks failed. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/NativeWiFi/wlan-reason-code">WLAN_REASON_CODE</a> data type value that identifies the reason the WLAN operation failed.

### -field wlan_notification_acm_connection_start

A connection has started  to a network in range.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt.

### -field wlan_notification_acm_connection_complete

A connection has completed.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt that completed. The connection succeeded if the <b>wlanReasonCode</b> in <b>WLAN_CONNECTION_NOTIFICATION_DATA</b> is <b>WLAN_REASON_CODE_SUCCESS</b>. Otherwise, the connection has failed.

### -field wlan_notification_acm_connection_attempt_fail

A connection attempt has failed.

A connection consists of one or more connection attempts. An application may receive zero or more <b>wlan_notification_acm_connection_attempt_fail </b> notifications between receiving the <b>wlan_notification_acm_connection_start</b> notification and the <b>wlan_notification_acm_connection_complete</b> notification.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt that failed.

### -field wlan_notification_acm_filter_list_change

A change in the filter list has occurred, either through group policy or a call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a> function. 

An application can call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a> function to retrieve the new filter list.

### -field wlan_notification_acm_interface_arrival

A wireless LAN interface is been added to or enabled on the local computer.

### -field wlan_notification_acm_interface_removal

A wireless LAN interface is been removed from or disabled on the local computer.

### -field wlan_notification_acm_profile_change

A change in a profile or the profile list has occurred, either through group policy or by calls to Native Wifi functions. 

An application can call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a> and <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a> functions to retrieve the updated profiles. The interface on which the profile list changes is identified by the <b>InterfaceGuid</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure.

### -field wlan_notification_acm_profile_name_change

A profile name has changed, either through group policy or by calls to Native Wifi functions. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a buffer that contains   two NULL-terminated WCHAR strings, the old profile name followed by the new profile name.

### -field wlan_notification_acm_profiles_exhausted

All profiles were exhausted in an attempt to autoconnect.

### -field wlan_notification_acm_network_not_available

The wireless service cannot find any connectable network after a scan. 

The interface on which no connectable network is found is identified by identified by the <b>InterfaceGuid</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure.

### -field wlan_notification_acm_network_available

The wireless service found a connectable network after a scan, the interface was in the disconnected state, and there is no compatible auto-connect profile that the wireless service can use to connect .

The interface on which connectable networks are found is identified by the <b>InterfaceGuid</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure.

### -field wlan_notification_acm_disconnecting

The wireless service is disconnecting from a  connectable network.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection that is disconnecting.

### -field wlan_notification_acm_disconnected

The wireless service has disconnected from a  connectable network.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection that disconnected.

### -field wlan_notification_acm_adhoc_network_state_change

A state change has occurred for an adhoc network. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_adhoc_network_state-r1">WLAN_ADHOC_NETWORK_STATE</a> enumeration value that identifies the new  adhoc network state.

### -field wlan_notification_acm_profile_unblocked

This value is supported on Windows 8 and later.

### -field wlan_notification_acm_screen_power_change

The screen power has changed. 

The <b>pData</b> member points to a  <b>BOOL</b> value that indicates the value of the screen power change. When this value is <b>TRUE</b>, the screen changed to on. When this value is <b>FALSE</b>, the screen changed to off. 

This value is supported on Windows 8 and later.

### -field wlan_notification_acm_profile_blocked

This value is supported on Windows 8 and later.

### -field wlan_notification_acm_scan_list_refresh

This value is supported on Windows 8 and later.

### -field wlan_notification_acm_operational_state_change

### -field wlan_notification_acm_end

Indicates the end of the range that specifies the possible values for ACM notifications.

## -remarks

The <b>WLAN_NOTIFICATION_ACM</b> enumerated type is used by the Auto Configuration Module, the new wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_NOTIFICATION_ACM</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_ACM</b>. 

The starting value for the <b>WLAN_NOTIFICATION_ACM</b> enumeration is defined as L2_NOTIFICATION_CODE_V2_BEGIN in the <i>l2cmn.h</i> header file.  Note that the <i>l2cmn.h</i> header is automatically included by the <i>wlanapi.h</i> header file.



The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_notification_acm_connection_complete</b> and <b>wlan_notification_acm_disconnected</b> notifications are available.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>

<a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a>

<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_adhoc_network_state-r1">WLAN_ADHOC_NETWORK_STATE</a>

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_notification_data">WLAN_CONNECTION_NOTIFICATION_DATA</a>

<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>

<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>

<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_power_setting-r1">WLAN_POWER_SETTING</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>
