---
UID: NE:dot1x._ONEX_AUTH_IDENTITY
title: ONEX_AUTH_IDENTITY (dot1x.h)
description: Specifies the possible values of the identity used for 802.1X authentication status.
helpviewer_keywords: ["ONEX_AUTH_IDENTITY","ONEX_AUTH_IDENTITY enumeration [NativeWIFI]","OneXAuthIdentityExplicitUser","OneXAuthIdentityGuest","OneXAuthIdentityInvalid","OneXAuthIdentityMachine","OneXAuthIdentityNone","OneXAuthIdentityUser","PONEX_AUTH_IDENTITY","PONEX_AUTH_IDENTITY enumeration pointer [NativeWIFI]","dot1x/ONEX_AUTH_IDENTITY","dot1x/OneXAuthIdentityExplicitUser","dot1x/OneXAuthIdentityGuest","dot1x/OneXAuthIdentityInvalid","dot1x/OneXAuthIdentityMachine","dot1x/OneXAuthIdentityNone","dot1x/OneXAuthIdentityUser","dot1x/PONEX_AUTH_IDENTITY","nwifi.onex_auth_identity"]
old-location: nwifi\onex_auth_identity.htm
tech.root: nwifi
ms.assetid: c51ab620-7e44-4798-8206-8ae9bbcd6614
ms.date: 12/05/2018
ms.keywords: ONEX_AUTH_IDENTITY, ONEX_AUTH_IDENTITY enumeration [NativeWIFI], OneXAuthIdentityExplicitUser, OneXAuthIdentityGuest, OneXAuthIdentityInvalid, OneXAuthIdentityMachine, OneXAuthIdentityNone, OneXAuthIdentityUser, PONEX_AUTH_IDENTITY, PONEX_AUTH_IDENTITY enumeration pointer [NativeWIFI], dot1x/ONEX_AUTH_IDENTITY, dot1x/OneXAuthIdentityExplicitUser, dot1x/OneXAuthIdentityGuest, dot1x/OneXAuthIdentityInvalid, dot1x/OneXAuthIdentityMachine, dot1x/OneXAuthIdentityNone, dot1x/OneXAuthIdentityUser, dot1x/PONEX_AUTH_IDENTITY, nwifi.onex_auth_identity
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
req.typenames: ONEX_AUTH_IDENTITY, PONEX_AUTH_IDENTITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_AUTH_IDENTITY
 - dot1x/_ONEX_AUTH_IDENTITY
 - ONEX_AUTH_IDENTITY
 - dot1x/ONEX_AUTH_IDENTITY
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
 - ONEX_AUTH_IDENTITY
---

# ONEX_AUTH_IDENTITY enumeration


## -description

The <b>ONEX_AUTH_IDENTITY</b> enumerated type specifies the possible values of  the identity used for 802.1X authentication status.

## -enum-fields

### -field OneXAuthIdentityNone

No identity is specified in the profile used for 802.1X authentication.

### -field OneXAuthIdentityMachine

The identity of the local machine account is used for 802.1X authentication.

### -field OneXAuthIdentityUser

The identity of the logged-on user is used for 802.1X authentication.

### -field OneXAuthIdentityExplicitUser

The identity of an explicit user as specified in the profile is used for 802.1X authentication. This value is used when performing single signon or when credentials are saved with the profile.

### -field OneXAuthIdentityGuest

The identity of the Guest account as specified in the profile is used for 802.1X authentication.

### -field OneXAuthIdentityInvalid

The identity is not valid as specified in the profile used for 802.1X authentication.

## -remarks

The <b>ONEX_AUTH_IDENTITY</b> enumerated type is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_AUTH_IDENTITY</b> specifies the possible values of the identity used for 802.1X authentication. The <b>ONEX_AUTH_IDENTITY</b> is a function of the
    802.1X authentication mode selected and various system triggers (user logon and logoff operations, for example).


The <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

If the <b>fOneXAuthParams</b> member in the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure is set, then the  <b>authParams</b> member of the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains an <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> structure with an <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params">ONEX_AUTH_PARAMS</a> structure embedded starting at the <b>dwOffset</b> member of the  <b>ONEX_VARIABLE_BLOB</b>. This <b>ONEX_AUTH_PARAMS</b>  structure that contains a value from the <b>ONEX_AUTH_IDENTITY</b> enumeration in the <b>authIdentity</b> member.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params">ONEX_AUTH_PARAMS</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>