---
UID: NE:dot1x._ONEX_NOTIFICATION_TYPE
title: ONEX_NOTIFICATION_TYPE (dot1x.h)
description: Specifies the possible values of the NotificationCode member of the WLAN_NOTIFICATION_DATA structure for 802.1X module notifications.
helpviewer_keywords: ["ONEX_NOTIFICATION_TYPE","ONEX_NOTIFICATION_TYPE enumeration [NativeWIFI]","OneXNotificationTypeAuthRestarted","OneXNotificationTypeEventInvalid","OneXNotificationTypeResultUpdate","OneXNumNotifications","OneXPublicNotificationBase","PONEX_NOTIFICATION_TYPE","PONEX_NOTIFICATION_TYPE enumeration pointer [NativeWIFI]","dot1x/ONEX_NOTIFICATION_TYPE","dot1x/OneXNotificationTypeAuthRestarted","dot1x/OneXNotificationTypeEventInvalid","dot1x/OneXNotificationTypeResultUpdate","dot1x/OneXNumNotifications","dot1x/OneXPublicNotificationBase","dot1x/PONEX_NOTIFICATION_TYPE","nwifi.onex_notification_type"]
old-location: nwifi\onex_notification_type.htm
tech.root: nwifi
ms.assetid: c5892938-9798-4c09-a766-4924cda4d090
ms.date: 12/05/2018
ms.keywords: ONEX_NOTIFICATION_TYPE, ONEX_NOTIFICATION_TYPE enumeration [NativeWIFI], OneXNotificationTypeAuthRestarted, OneXNotificationTypeEventInvalid, OneXNotificationTypeResultUpdate, OneXNumNotifications, OneXPublicNotificationBase, PONEX_NOTIFICATION_TYPE, PONEX_NOTIFICATION_TYPE enumeration pointer [NativeWIFI], dot1x/ONEX_NOTIFICATION_TYPE, dot1x/OneXNotificationTypeAuthRestarted, dot1x/OneXNotificationTypeEventInvalid, dot1x/OneXNotificationTypeResultUpdate, dot1x/OneXNumNotifications, dot1x/OneXPublicNotificationBase, dot1x/PONEX_NOTIFICATION_TYPE, nwifi.onex_notification_type
req.header: dot1x.h
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
req.typenames: ONEX_NOTIFICATION_TYPE, PONEX_NOTIFICATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_NOTIFICATION_TYPE
 - dot1x/_ONEX_NOTIFICATION_TYPE
 - ONEX_NOTIFICATION_TYPE
 - dot1x/ONEX_NOTIFICATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dot1x.h
api_name:
 - ONEX_NOTIFICATION_TYPE
---

# ONEX_NOTIFICATION_TYPE enumeration


## -description

The <b>ONEX_NOTIFICATION_TYPE</b> enumerated type specifies the possible values of the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for 802.1X module notifications.

## -enum-fields

### -field OneXPublicNotificationBase:0

Indicates the beginning of the range that specifies the possible values for 802.1X notifications.

### -field OneXNotificationTypeResultUpdate

Indicates that 802.1X authentication has a status change.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to a  <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure that contains 802.1X update data.

### -field OneXNotificationTypeAuthRestarted

Indicates that 802.1X authentication restarted.

The <b>pData</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure points to an  <a href="/windows/desktop/api/dot1x/ne-dot1x-onex_auth_restart_reason">ONEX_AUTH_RESTART_REASON</a> enumeration value that identifies the reason the authentication was restarted.

### -field OneXNotificationTypeEventInvalid

Indicates the end of the range that specifies the possible values for 802.1X notifications.

### -field OneXNumNotifications

Indicates the end of the range that specifies the possible values for 802.1X notifications.

## -remarks

The <b>ONEX_NOTIFICATION_TYPE</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_NOTIFICATION_TYPE</b> specifies the possible values for the <b>NotificationCode</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure for received notifications  when the <b>NotificationSource</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>. 

The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function is used by an application to register and unregister notifications on all wireless interfaces. When registering for notifications, an application must provide a callback function pointed to by the <i>funcCallback</i> parameter passed to the <b>WlanRegisterNotification</b> function. The prototype for this callback function is the <a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>. This callback function will receive notifications that have been registered in the <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function. 

The callback function is called with a pointer to a <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure as the first parameter that contains detailed information on the notification. The callback function also receives a second parameter that contains a pointer to the client context passed in the <i>pCallbackContext</i> parameter to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function. This client context can be a <b>NULL</b> pointer if that is what was passed to the <b>WlanRegisterNotification</b> function.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_auth_restart_reason">ONEX_AUTH_RESTART_REASON</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wlan_notification_callback">WLAN_NOTIFICATION_CALLBACK</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>
