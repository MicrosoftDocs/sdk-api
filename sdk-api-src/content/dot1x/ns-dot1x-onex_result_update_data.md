---
UID: NS:dot1x._ONEX_RESULT_UPDATE_DATA
title: ONEX_RESULT_UPDATE_DATA (dot1x.h)
description: Contains information on a status change to 802.1X authentication.
helpviewer_keywords: ["*PONEX_RESULT_UPDATE_DATA","ONEX_RESULT_UPDATE_DATA","ONEX_RESULT_UPDATE_DATA structure [NativeWIFI]","PONEX_RESULT_UPDATE_DATA","PONEX_RESULT_UPDATE_DATA structure pointer [NativeWIFI]","dot1x/ONEX_RESULT_UPDATE_DATA","dot1x/PONEX_RESULT_UPDATE_DATA","nwifi.onex_result_update_data"]
old-location: nwifi\onex_result_update_data.htm
tech.root: nwifi
ms.assetid: 140386c8-2e35-4e83-812f-119bf8828d0b
ms.date: 12/05/2018
ms.keywords: '*PONEX_RESULT_UPDATE_DATA, ONEX_RESULT_UPDATE_DATA, ONEX_RESULT_UPDATE_DATA structure [NativeWIFI], PONEX_RESULT_UPDATE_DATA, PONEX_RESULT_UPDATE_DATA structure pointer [NativeWIFI], dot1x/ONEX_RESULT_UPDATE_DATA, dot1x/PONEX_RESULT_UPDATE_DATA, nwifi.onex_result_update_data'
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
req.typenames: ONEX_RESULT_UPDATE_DATA, *PONEX_RESULT_UPDATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_RESULT_UPDATE_DATA
 - dot1x/_ONEX_RESULT_UPDATE_DATA
 - PONEX_RESULT_UPDATE_DATA
 - dot1x/PONEX_RESULT_UPDATE_DATA
 - ONEX_RESULT_UPDATE_DATA
 - dot1x/ONEX_RESULT_UPDATE_DATA
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
 - ONEX_RESULT_UPDATE_DATA
---

# ONEX_RESULT_UPDATE_DATA structure


## -description

The <b>ONEX_RESULT_UPDATE_DATA</b> structure contains information on a status change to 802.1X authentication.

## -struct-fields

### -field oneXStatus

Specifies the current 802.1X authentication status. For more information, see the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_status">ONEX_STATUS</a> structure.

### -field BackendSupport

Indicates if the configured EAP method on the supplicant is supported on the 802.1X authentication server.

EAP permits the use of a backend
   authentication server, which may implement some or all authentication
   methods, with the authenticator acting as a pass-through for some or
   all methods and peers. For more information, see RFC 3748 published by the IETF and the <a href="/windows/desktop/api/dot1x/ne-dot1x-onex_eap_method_backend_support">ONEX_EAP_METHOD_BACKEND_SUPPORT</a> enumeration.

### -field fBackendEngaged

Indicates if a response was received from the 802.1X authentication server.

### -field fOneXAuthParams

Indicates if the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains 802.1X authentication parameters in the <b>authParams</b> member.

### -field fEapError

Indicates if the <b>ONEX_RESULT_UPDATE_DATA</b> structure contains an EAP error in the <b>eapError</b> member.

### -field authParams

The 802.1X authentication parameters. This member contains an embedded <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params">ONEX_AUTH_PARAMS</a> structure starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fOneXAuthParams</b> bitfield member is set.

### -field eapError

An EAP error value. This member contains an embedded <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_eap_error">ONEX_EAP_ERROR</a> structure starting at the <b>dwOffset</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a> if the <b>fEapError</b> bitfield member is set.

## -remarks

The <b>ONEX_RESULT_UPDATE_DATA</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <b>ONEX_RESULT_UPDATE_DATA</b> contains information on a status change to 802.1X authentication.This structure is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params">ONEX_AUTH_PARAMS</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_eap_error">ONEX_EAP_ERROR</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_eap_method_backend_support">ONEX_EAP_METHOD_BACKEND_SUPPORT</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type">ONEX_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_status">ONEX_STATUS</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob">ONEX_VARIABLE_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>