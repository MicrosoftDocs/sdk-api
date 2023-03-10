---
UID: NE:wlanapi._WLAN_NOTIFICATION_MSM~r1
title: WLAN_NOTIFICATION_MSM
description: The WLAN_NOTIFICATION_MSM enumeration specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure.
ms.date: 08/16/2022
ms.keywords: _WLAN_NOTIFICATION_MSM, WLAN_NOTIFICATION_MSM
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
 - _WLAN_NOTIFICATION_MSM
 - wlanapi/_WLAN_NOTIFICATION_MSM
 - PWLAN_NOTIFICATION_MSM
 - wlanapi/PWLAN_NOTIFICATION_MSM
 - WLAN_NOTIFICATION_MSM
 - wlanapi/WLAN_NOTIFICATION_MSM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_NOTIFICATION_MSM
 - WLAN_NOTIFICATION_MSM
---

# WLAN_NOTIFICATION_MSM enumeration


## -description

The <b>WLAN_NOTIFICATION_MSM</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for Media Specific Module  (MSM) notifications.

## -enum-fields

### -field wlan_notification_msm_start

The beginning of the range that specifies the possible values for ACM notifications.

### -field wlan_notification_msm_associating

A wireless device is in the process of associating with an access point or a peer station. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_associated

The wireless device has associated with an access point or a peer station.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_authenticating

The wireless device is in the process of authenticating.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_connected

The wireless device is associated with an access point or a peer station, keys have been exchanged, and the wireless device is available to send data. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_roaming_start

The wireless device is connected to an access point and has initiated roaming to another access point.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_roaming_end

The wireless device was connected to an access point and has completed roaming to another access point.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_radio_state_change

The radio state for an adapter has changed. Each physical layer (PHY) has its own radio state. The radio for an adapter is switched off when the radio state of every PHY is off.  

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_phy_radio_state">WLAN_PHY_RADIO_STATE</a> structure that identifies the new radio state.

### -field wlan_notification_msm_signal_quality_change

A signal quality change for the currently associated access point or peer station.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a ULONG WLAN_SIGNAL_QUALITY that identifies  the new signal quality.

### -field wlan_notification_msm_disassociating

A wireless device is in the process of disassociating from an access point or a peer station. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_disconnected

The wireless device is not associated with an access point or a peer station. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information. The <b>wlanReasonCode</b> member of the <b>WLAN_MSM_NOTIFICATION_DATA</b> structure  indicates the reason for the disconnect.

### -field wlan_notification_msm_peer_join

A peer has joined an adhoc network.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_peer_leave

A peer has left an adhoc network.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_adapter_removal

A wireless adapter has been removed from the local computer. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a> structure that contains connection-related information.

### -field wlan_notification_msm_adapter_operation_mode_change

The operation mode of the wireless device has changed. 

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a ULONG that identifies the new operation mode.

### -field wlan_notification_msm_link_degraded

### -field wlan_notification_msm_link_improved

### -field wlan_notification_msm_end

Indicates the end of the range that specifies the possible values for MSM notifications.

## -remarks

The <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_notification_acm-r1">WLAN_NOTIFICATION_ACM</a> enumerated type is used by the Media Specific Module, the new wireless configuration component supported on Windows Vista and  later.  

The <b>WLAN_NOTIFICATION_MSM</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_MSM</b>. 

The starting value for the <b>WLAN_NOTIFICATION_MSM</b> enumeration is defined as L2_NOTIFICATION_CODE_PUBLIC_BEGIN in the <i>l2cmn.h</i> header file.  Note that the <i>l2cmn.h</i> header is automatically included by the <i>wlanapi.h</i> header file.



The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_msm_notification_data">WLAN_MSM_NOTIFICATION_DATA</a>

<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>

<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>
