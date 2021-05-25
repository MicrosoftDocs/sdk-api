---
UID: NE:dot1x._ONEX_AUTH_RESTART_REASON
title: ONEX_AUTH_RESTART_REASON (dot1x.h)
description: Specifies the possible reasons that 802.1X authentication was restarted.
helpviewer_keywords: ["ONEX_AUTH_RESTART_REASON","ONEX_AUTH_RESTART_REASON enumeration [NativeWIFI]","OneXRestartReasonAltCredsTrial","OneXRestartReasonInvalid","OneXRestartReasonMsmInitiated","OneXRestartReasonOneXAuthTimeout","OneXRestartReasonOneXConfigurationChanged","OneXRestartReasonOneXHeldStateTimeout","OneXRestartReasonOneXUserChanged","OneXRestartReasonPeerInitiated","OneXRestartReasonQuarantineStateChanged","PONEX_AUTH_RESTART_REASON","PONEX_AUTH_RESTART_REASON enumeration pointer [NativeWIFI]","dot1x/ONEX_AUTH_RESTART_REASON","dot1x/OneXRestartReasonAltCredsTrial","dot1x/OneXRestartReasonInvalid","dot1x/OneXRestartReasonMsmInitiated","dot1x/OneXRestartReasonOneXAuthTimeout","dot1x/OneXRestartReasonOneXConfigurationChanged","dot1x/OneXRestartReasonOneXHeldStateTimeout","dot1x/OneXRestartReasonOneXUserChanged","dot1x/OneXRestartReasonPeerInitiated","dot1x/OneXRestartReasonQuarantineStateChanged","dot1x/PONEX_AUTH_RESTART_REASON","nwifi.onex_auth_restart_reason"]
old-location: nwifi\onex_auth_restart_reason.htm
tech.root: nwifi
ms.assetid: 794231da-ef4e-4419-9ff8-9b23483853d1
ms.date: 12/05/2018
ms.keywords: ONEX_AUTH_RESTART_REASON, ONEX_AUTH_RESTART_REASON enumeration [NativeWIFI], OneXRestartReasonAltCredsTrial, OneXRestartReasonInvalid, OneXRestartReasonMsmInitiated, OneXRestartReasonOneXAuthTimeout, OneXRestartReasonOneXConfigurationChanged, OneXRestartReasonOneXHeldStateTimeout, OneXRestartReasonOneXUserChanged, OneXRestartReasonPeerInitiated, OneXRestartReasonQuarantineStateChanged, PONEX_AUTH_RESTART_REASON, PONEX_AUTH_RESTART_REASON enumeration pointer [NativeWIFI], dot1x/ONEX_AUTH_RESTART_REASON, dot1x/OneXRestartReasonAltCredsTrial, dot1x/OneXRestartReasonInvalid, dot1x/OneXRestartReasonMsmInitiated, dot1x/OneXRestartReasonOneXAuthTimeout, dot1x/OneXRestartReasonOneXConfigurationChanged, dot1x/OneXRestartReasonOneXHeldStateTimeout, dot1x/OneXRestartReasonOneXUserChanged, dot1x/OneXRestartReasonPeerInitiated, dot1x/OneXRestartReasonQuarantineStateChanged, dot1x/PONEX_AUTH_RESTART_REASON, nwifi.onex_auth_restart_reason
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
req.typenames: ONEX_AUTH_RESTART_REASON, PONEX_AUTH_RESTART_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_AUTH_RESTART_REASON
 - dot1x/_ONEX_AUTH_RESTART_REASON
 - ONEX_AUTH_RESTART_REASON
 - dot1x/ONEX_AUTH_RESTART_REASON
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
 - ONEX_AUTH_RESTART_REASON
---

# ONEX_AUTH_RESTART_REASON enumeration


## -description

The <b>ONEX_AUTH_RESTART_REASON</b> enumerated type specifies the possible reasons that 802.1X authentication was restarted.

## -enum-fields

### -field OneXRestartReasonPeerInitiated

The EAPHost component (the peer) requested the 802.1x module to restart 802.1X authentication. This results from a <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerProcessReceivedPacket</a> function call that returns an <a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a> enumeration value of <b>EapHostPeerResponseStartAuthentication</b> in the <i>pEapOutput</i> parameter.

### -field OneXRestartReasonMsmInitiated

The Media Specific Module (MSM) initiated the 802.1X authentication restart.

### -field OneXRestartReasonOneXHeldStateTimeout

The 802.1X authentication restart was the result of a state timeout. The timer expiring is the heldWhile timer of the 802.1X supplicant state machine defined in IEEE 802.1X - 2004 standard for Port-Based Network Access Control. The heldWhile timer is used by the supplicant state machine to define periods of time during which it
will not attempt to acquire an authenticator.

### -field OneXRestartReasonOneXAuthTimeout

The 802.1X authentication restart was the result of a state timeout. The timer expiring is the authWhile timer of the 802.1X supplicant port access entity defined in IEEE 802.1X - 2004 standard for Port-Based Network Access Control. The authWhile timer is used by the supplicant port access entity to determine how long to wait for a request from
the authenticator before timing it out.

### -field OneXRestartReasonOneXConfigurationChanged

The 802.1X authentication restart was the result of a configuration change to the current profile.

### -field OneXRestartReasonOneXUserChanged

The 802.1X authentication restart was the result of a change of user. This could occur if the current user logs off and new user logs on to the local computer.

### -field OneXRestartReasonQuarantineStateChanged

The 802.1X authentication restart was the result of receiving a notification from the EAP quarantine enforcement client (QEC) due to a network health change. If an EAPHost supplicant is participating in network access protection (NAP), the supplicant will respond to changes in the state of its network health. If that state changes, the supplicant must then initiate a re-authentication session. For more information, see the <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a> function.

### -field OneXRestartReasonAltCredsTrial

The 802.1X authentication restart was caused by a new authentication attempt with alternate user credentials. EAP methods like MSCHAPv2 prefer to use logged-on user credentials for 802.1X authentication. If these user credentials do not work, then a dialog will be displayed to the user that asks permission to use alternate credentials for 802.1X authentication. For more information, see the <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a> function and EAP_FLAG_PREFER_ALT_CREDENTIALS flag in the <i>dwflags</i> parameter.

### -field OneXRestartReasonInvalid

Indicates the end of the range that specifies the possible reasons that 802.1X authentication was restarted.

## -remarks

The <b>ONEX_AUTH_RESTART_REASON</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_AUTH_RESTART_REASON</b> specifies the possible values for the reason that 802.1X authentication was restarted. A value from this enumeration is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notifications  is <b>OneXNotificationTypeAuthRestarted</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_AUTH_RESTART_REASON</b> enumeration value that identifies the reason the authentication was restarted.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket">EapHostPeerProcessReceivedPacket</a>



<a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>