---
UID: NS:dot1x._ONEX_AUTH_PARAMS
title: ONEX_AUTH_PARAMS (dot1x.h)
description: Contains 802.1X authentication parameters used for 802.1X authentication.
helpviewer_keywords: ["*PONEX_AUTH_PARAMS","ONEX_AUTH_PARAMS","ONEX_AUTH_PARAMS structure [NativeWIFI]","PONEX_AUTH_PARAMS","PONEX_AUTH_PARAMS structure pointer [NativeWIFI]","dot1x/ONEX_AUTH_PARAMS","dot1x/PONEX_AUTH_PARAMS","nwifi.onex_auth_params"]
old-location: nwifi\onex_auth_params.htm
tech.root: nwifi
ms.assetid: a5dcd546-abe5-4553-baa8-656d37b263a3
ms.date: 12/05/2018
ms.keywords: '*PONEX_AUTH_PARAMS, ONEX_AUTH_PARAMS, ONEX_AUTH_PARAMS structure [NativeWIFI], PONEX_AUTH_PARAMS, PONEX_AUTH_PARAMS structure pointer [NativeWIFI], dot1x/ONEX_AUTH_PARAMS, dot1x/PONEX_AUTH_PARAMS, nwifi.onex_auth_params'
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
req.typenames: ONEX_AUTH_PARAMS, *PONEX_AUTH_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_AUTH_PARAMS
 - dot1x/_ONEX_AUTH_PARAMS
 - PONEX_AUTH_PARAMS
 - dot1x/PONEX_AUTH_PARAMS
 - ONEX_AUTH_PARAMS
 - dot1x/ONEX_AUTH_PARAMS
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
 - ONEX_AUTH_PARAMS
---

# ONEX_AUTH_PARAMS structure


## -description

The <b>ONEX_AUTH_PARAMS</b> structure contains 802.1X authentication parameters used for 802.1X authentication.

## -struct-fields

### -field fUpdatePending

Indicates if a status update is pending for 802.X authentication.

### -field oneXConnProfile

The 802.1X authentication connection profile. This member contains an embedded <a href="/windows/desktop/NativeWiFi/onex-connection-profile">ONEX_CONNECTION_PROFILE</a> structure starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a>.

### -field authIdentity

The identity used for 802.1X authentication status. This member is a value from the <a href="/windows/desktop/api/dot1x/ne-dot1x-onex_auth_identity">ONEX_AUTH_IDENTITY</a> enumeration.

### -field dwQuarantineState

The quarantine isolation state value of the local computer. The isolation state determines its network connectivity. This member corresponds to a value from the EAPHost <a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state">ISOLATION_STATE</a> enumeration.

### -field fSessionId

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a session ID in the <b>dwSessionId</b> member.

### -field fhUserToken

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a user token handle in the <b>hUserToken</b> member. 

For security reasons, the <b>hUserToken</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.

### -field fOnexUserProfile

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains an 802.1X user profile in the <b>OneXUserProfile</b> member.

For security reasons, the <b>OneXUserProfile</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.

### -field fIdentity

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains an 802.1X identity in the <b>Identity</b> member.

### -field fUserName

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a user name used for 802.1X authentication in the <b>UserName</b> member.

### -field fDomain

Indicates if the <b>ONEX_AUTH_PARAMS</b> structure contains a domain used for 802.1X authentication in the <b>Domain</b> member.

### -field dwSessionId

The session ID of the user currently logged on to the console. This member corresponds to the value returned by the <a href="/windows/desktop/api/winbase/nf-winbase-wtsgetactiveconsolesessionid">WTSGetActiveConsoleSessionId</a> function. This member contains a session ID if the <b>fSessionId</b> bitfield member is set.

### -field hUserToken

The user token handle  used for 802.1X authentication. This member contains a user token handle if the <b>fhUserToken</b> bitfield member is set.

For security reasons, the <b>hUserToken</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.

### -field OneXUserProfile

The 802.1X user profile used for 802.1X authentication. This member contains an embedded user profile starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fOneXUserProfile</b> bitfield member is set. 

For security reasons, the <b>OneXUserProfile</b> member of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is always set to <b>NULL</b>.

### -field Identity

The 802.1X identity used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the identity starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fIdentity</b> bitfield member is set.

### -field UserName

The user name used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the user name starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fUserName</b> bitfield member is set.

### -field Domain

The domain used for 802.1X authentication. This member contains a NULL-terminated Unicode string with the domain starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fDomain</b> bitfield member is set.

## -remarks

The <b>ONEX_AUTH_PARAMS</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

If the <b>fOneXAuthParams</b> member in the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is set, then the  <b>authParams</b> member of the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains an <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> structure with an <b>ONEX_AUTH_PARAMS</b> structure embedded starting at the <b>dwOffset</b> member of the  <b>ONEX_VARIABLE_BLOB</b>.

For security reasons, the <b>hUserToken</b> and <b>OneXUserProfile</b> members of the <b>ONEX_AUTH_PARAMS</b> structure returned in the <b>authParams</b> member are always set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state">ISOLATION_STATE</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_auth_identity">ONEX_AUTH_IDENTITY</a>



<b>ONEX_EAP_ERROR</b>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type">ONEX_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/winbase/nf-winbase-wtsgetactiveconsolesessionid">WTSGetActiveConsoleSessionId</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>