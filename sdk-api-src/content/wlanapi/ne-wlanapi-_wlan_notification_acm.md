---
UID: NE:wlanapi._WLAN_NOTIFICATION_ACM
title: "_WLAN_NOTIFICATION_ACM"
author: windows-sdk-content
description: Specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure for Auto Configuration Module (ACM) notifications.
old-location: nwifi\wlan_notification_acm.htm
tech.root: NativeWiFi
ms.assetid: b0814b2a-ccdc-4bf1-b11e-25f2cf6ba9bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_NOTIFICATION_ACM, PWLAN_NOTIFICATION_ACM, PWLAN_NOTIFICATION_ACM enumeration pointer [NativeWIFI], WLAN_NOTIFICATION_ACM, WLAN_NOTIFICATION_ACM enumeration [NativeWIFI], _WLAN_NOTIFICATION_ACM, nwifi.wlan_notification_acm, wlan_notification_acm_adhoc_network_state_change, wlan_notification_acm_autoconf_disabled, wlan_notification_acm_autoconf_enabled, wlan_notification_acm_background_scan_disabled, wlan_notification_acm_background_scan_enabled, wlan_notification_acm_bss_type_change, wlan_notification_acm_connection_attempt_fail, wlan_notification_acm_connection_complete, wlan_notification_acm_connection_start, wlan_notification_acm_disconnected, wlan_notification_acm_disconnecting, wlan_notification_acm_end, wlan_notification_acm_filter_list_change, wlan_notification_acm_interface_arrival, wlan_notification_acm_interface_removal, wlan_notification_acm_network_available, wlan_notification_acm_network_not_available, wlan_notification_acm_power_setting_change, wlan_notification_acm_profile_blocked, wlan_notification_acm_profile_change, wlan_notification_acm_profile_name_change, wlan_notification_acm_profile_unblocked, wlan_notification_acm_profiles_exhausted, wlan_notification_acm_scan_complete, wlan_notification_acm_scan_fail, wlan_notification_acm_scan_list_refresh, wlan_notification_acm_screen_power_change, wlan_notification_acm_start, wlanapi/PWLAN_NOTIFICATION_ACM, wlanapi/WLAN_NOTIFICATION_ACM, wlanapi/wlan_notification_acm_adhoc_network_state_change, wlanapi/wlan_notification_acm_autoconf_disabled, wlanapi/wlan_notification_acm_autoconf_enabled, wlanapi/wlan_notification_acm_background_scan_disabled, wlanapi/wlan_notification_acm_background_scan_enabled, wlanapi/wlan_notification_acm_bss_type_change, wlanapi/wlan_notification_acm_connection_attempt_fail, wlanapi/wlan_notification_acm_connection_complete, wlanapi/wlan_notification_acm_connection_start, wlanapi/wlan_notification_acm_disconnected, wlanapi/wlan_notification_acm_disconnecting, wlanapi/wlan_notification_acm_end, wlanapi/wlan_notification_acm_filter_list_change, wlanapi/wlan_notification_acm_interface_arrival, wlanapi/wlan_notification_acm_interface_removal, wlanapi/wlan_notification_acm_network_available, wlanapi/wlan_notification_acm_network_not_available, wlanapi/wlan_notification_acm_power_setting_change, wlanapi/wlan_notification_acm_profile_blocked, wlanapi/wlan_notification_acm_profile_change, wlanapi/wlan_notification_acm_profile_name_change, wlanapi/wlan_notification_acm_profile_unblocked, wlanapi/wlan_notification_acm_profiles_exhausted, wlanapi/wlan_notification_acm_scan_complete, wlanapi/wlan_notification_acm_scan_fail, wlanapi/wlan_notification_acm_scan_list_refresh, wlanapi/wlan_notification_acm_screen_power_change, wlanapi/wlan_notification_acm_start"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - Wlanapi.h
api_name:
 - WLAN_NOTIFICATION_ACM
product: Windows
targetos: Windows
req.typenames: WLAN_NOTIFICATION_ACM, *PWLAN_NOTIFICATION_ACM
req.redist: Wireless LAN API for Windows XP with SP2
---

# _WLAN_NOTIFICATION_ACM enumeration


## -description


The <b>WLAN_NOTIFICATION_ACM</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for Auto Configuration Module  (ACM) notifications.


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

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/13d57339-655e-4978-974e-e7b12a83d18a">DOT11_BSS_TYPE</a> enumeration value that identifies the new basic service set (BSS) type.


### -field wlan_notification_acm_power_setting_change

The power setting for an interface has changed.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/f2509c87-8a2a-4e6e-9995-e824a17e7083">WLAN_POWER_SETTING</a> enumeration value that identifies the new power setting of an interface.


### -field wlan_notification_acm_scan_complete

A scan for networks has completed.


### -field wlan_notification_acm_scan_fail

A scan for connectable networks failed. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a> data type value that identifies the reason the WLAN operation failed.


### -field wlan_notification_acm_connection_start

A connection has started  to a network in range.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt.


### -field wlan_notification_acm_connection_complete

A connection has completed.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt that completed. The connection succeeded if the <b>wlanReasonCode</b> in <b>WLAN_CONNECTION_NOTIFICATION_DATA</b> is <b>WLAN_REASON_CODE_SUCCESS</b>. Otherwise, the connection has failed.


### -field wlan_notification_acm_connection_attempt_fail

A connection attempt has failed.

A connection consists of one or more connection attempts. An application may receive zero or more <b>wlan_notification_acm_connection_attempt_fail </b>notifications between receiving the <b>wlan_notification_acm_connection_start</b> notification and the <b>wlan_notification_acm_connection_complete</b> notification.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection attempt that failed. 


### -field wlan_notification_acm_filter_list_change

A change in the filter list has occurred, either through group policy or a call to the <a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a> function. 

An application can call the <a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a> function to retrieve the new filter list.   


### -field wlan_notification_acm_interface_arrival

A wireless LAN interface is been added to or enabled on the local computer.


### -field wlan_notification_acm_interface_removal

A wireless LAN interface is been removed from or disabled on the local computer.


### -field wlan_notification_acm_profile_change

A change in a profile or the profile list has occurred, either through group policy or by calls to Native Wifi functions. 

An application can call the <a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a> and <a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a> functions to retrieve the updated profiles. The interface on which the profile list changes is identified by the <b>InterfaceGuid</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure.


### -field wlan_notification_acm_profile_name_change

A profile name has changed, either through group policy or by calls to Native Wifi functions. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a buffer that contains   two NULL-terminated WCHAR strings, the old profile name followed by the new profile name.


### -field wlan_notification_acm_profiles_exhausted

All profiles were exhausted in an attempt to autoconnect.


### -field wlan_notification_acm_network_not_available

The wireless service cannot find any connectable network after a scan. 

The interface on which no connectable network is found is identified by identified by the <b>InterfaceGuid</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure.


### -field wlan_notification_acm_network_available

The wireless service found a connectable network after a scan, the interface was in the disconnected state, and there is no compatible auto-connect profile that the wireless service can use to connect .

The interface on which connectable networks are found is identified by the <b>InterfaceGuid</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure.


### -field wlan_notification_acm_disconnecting

The wireless service is disconnecting from a  connectable network.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection that is disconnecting.


### -field wlan_notification_acm_disconnected

The wireless service has disconnected from a  connectable network.

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a> structure that identifies the network  information for the connection that disconnected.


### -field wlan_notification_acm_adhoc_network_state_change

A state change has occurred for an adhoc network. 

The <b>pData</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="https://msdn.microsoft.com/9f233e3b-6905-4b6b-84b4-202076d224f5">WLAN_ADHOC_NETWORK_STATE</a> enumeration value that identifies the new  adhoc network state.


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


### -field v1_enum




## -remarks



The <b>WLAN_NOTIFICATION_ACM</b> enumerated type is used by the Auto Configuration Module, the new wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_NOTIFICATION_ACM</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_ACM</b>. 

The starting value for the <b>WLAN_NOTIFICATION_ACM</b> enumeration is defined as L2_NOTIFICATION_CODE_V2_BEGIN in the <i>l2cmn.h</i> header file.  Note that the <i>l2cmn.h</i> header is automatically included by the <i>wlanapi.h</i> header file.



The <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_notification_acm_connection_complete</b> and <b>wlan_notification_acm_disconnected</b> notifications are available.




## -see-also




<a href="https://msdn.microsoft.com/4a5c0085-0e7b-424d-9205-5ec39518a088">About the ACM Architecture</a>



<a href="https://msdn.microsoft.com/13d57339-655e-4978-974e-e7b12a83d18a">DOT11_BSS_TYPE</a>



<a href="https://msdn.microsoft.com/9f233e3b-6905-4b6b-84b4-202076d224f5">WLAN_ADHOC_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/df721e77-3285-442b-aabd-2dccae85fda5">WLAN_NOTIFICATION_CALLBACK</a>



<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/f2509c87-8a2a-4e6e-9995-e824a17e7083">WLAN_POWER_SETTING</a>



<a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>



<a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a>
 

 

