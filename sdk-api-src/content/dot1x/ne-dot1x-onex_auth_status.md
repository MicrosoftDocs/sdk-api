---
UID: NE:dot1x._ONEX_AUTH_STATUS
title: ONEX_AUTH_STATUS (dot1x.h)
description: Specifies the possible values for the 802.1X authentication status.
helpviewer_keywords: ["ONEX_AUTH_STATUS","ONEX_AUTH_STATUS enumeration [NativeWIFI]","OneXAuthFailure","OneXAuthInProgress","OneXAuthInvalid","OneXAuthNoAuthenticatorFound","OneXAuthNotStarted","OneXAuthSuccess","PONEX_AUTH_STATUS","PONEX_AUTH_STATUS enumeration pointer [NativeWIFI]","dot1x/ONEX_AUTH_STATUS","dot1x/OneXAuthFailure","dot1x/OneXAuthInProgress","dot1x/OneXAuthInvalid","dot1x/OneXAuthNoAuthenticatorFound","dot1x/OneXAuthNotStarted","dot1x/OneXAuthSuccess","dot1x/PONEX_AUTH_STATUS","nwifi.onex_auth_status"]
old-location: nwifi\onex_auth_status.htm
tech.root: nwifi
ms.assetid: 9a5c7876-2c6b-450e-95e4-2766d63b6e19
ms.date: 12/05/2018
ms.keywords: ONEX_AUTH_STATUS, ONEX_AUTH_STATUS enumeration [NativeWIFI], OneXAuthFailure, OneXAuthInProgress, OneXAuthInvalid, OneXAuthNoAuthenticatorFound, OneXAuthNotStarted, OneXAuthSuccess, PONEX_AUTH_STATUS, PONEX_AUTH_STATUS enumeration pointer [NativeWIFI], dot1x/ONEX_AUTH_STATUS, dot1x/OneXAuthFailure, dot1x/OneXAuthInProgress, dot1x/OneXAuthInvalid, dot1x/OneXAuthNoAuthenticatorFound, dot1x/OneXAuthNotStarted, dot1x/OneXAuthSuccess, dot1x/PONEX_AUTH_STATUS, nwifi.onex_auth_status
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
req.typenames: ONEX_AUTH_STATUS, PONEX_AUTH_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_AUTH_STATUS
 - dot1x/_ONEX_AUTH_STATUS
 - ONEX_AUTH_STATUS
 - dot1x/ONEX_AUTH_STATUS
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
 - ONEX_AUTH_STATUS
---

# ONEX_AUTH_STATUS enumeration


## -description

The <b>ONEX_AUTH_STATUS</b> enumerated type specifies the possible values for  the 802.1X authentication status.

## -enum-fields

### -field OneXAuthNotStarted

802.1X authentication was not started.

### -field OneXAuthInProgress

802.1X authentication is in progress.

### -field OneXAuthNoAuthenticatorFound

No 802.1X authenticator was found. The 802.1X authentication was attempted, but no 802.1X peer was found. In this case, either  the network does not support or is not configured to support the 802.1X standard.

### -field OneXAuthSuccess

802.1X authentication was successful.

### -field OneXAuthFailure

802.1X authentication was a failure.

### -field OneXAuthInvalid

Indicates the end of the range that specifies the possible values for 802.1X authentication status.

## -remarks

The <b>ONEX_AUTH_STATUS</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_AUTH_STATUS</b> specifies the possible values for the 802.1X authentication status. A value from this enumeration is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notifications  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure that contains a <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_status">ONEX_STATUS</a>  structure member in the <b>oneXStatus</b> structure member. The <b>ONEX_STATUS</b>  structure contains a <b>ONEX_AUTH_STATUS</b> enumeration value in the <b>authStatus</b> member.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_status">ONEX_STATUS</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>