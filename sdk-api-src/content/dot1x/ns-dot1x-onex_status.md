---
UID: NS:dot1x._ONEX_STATUS
title: ONEX_STATUS (dot1x.h)
description: Contains the current 802.1X authentication status.
helpviewer_keywords: ["*PONEX_STATUS","ONEX_STATUS","ONEX_STATUS structure [NativeWIFI]","PONEX_STATUS","PONEX_STATUS structure pointer [NativeWIFI]","dot1x/ONEX_STATUS","dot1x/PONEX_STATUS","nwifi.onex_status"]
old-location: nwifi\onex_status.htm
tech.root: nwifi
ms.assetid: 2c19c65b-0943-4561-a28f-0104e1cbd229
ms.date: 12/05/2018
ms.keywords: '*PONEX_STATUS, ONEX_STATUS, ONEX_STATUS structure [NativeWIFI], PONEX_STATUS, PONEX_STATUS structure pointer [NativeWIFI], dot1x/ONEX_STATUS, dot1x/PONEX_STATUS, nwifi.onex_status'
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
req.typenames: ONEX_STATUS, *PONEX_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_STATUS
 - dot1x/_ONEX_STATUS
 - PONEX_STATUS
 - dot1x/PONEX_STATUS
 - ONEX_STATUS
 - dot1x/ONEX_STATUS
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
 - ONEX_STATUS
---

# ONEX_STATUS structure


## -description

The <b>ONEX_STATUS</b> structure contains the current 802.1X authentication status.

## -struct-fields

### -field authStatus

The current status of the 802.1X authentication process. Any error that may have occurred during authentication is indicated below by the value of the <b>dwReason</b> and <b>dwError</b> members of the <b>ONEX_STATUS</b> structure. For more information, see the <a href="/windows/desktop/api/dot1x/ne-dot1x-onex_auth_status">ONEX_AUTH_STATUS</a> enumeration.

### -field dwReason

If an error occurred during 802.1X authentication, this member contains the reason for the error specified as a value from the <a href="/windows/desktop/api/dot1x/ne-dot1x-onex_reason_code">ONEX_REASON_CODE</a> enumeration. This member is normally <b>ONEX_REASON_CODE_SUCCESS</b> 
 when 802.1X authentication is successful and no error occurs.

### -field dwError

If an error occurred during 802.1X authentication, this member contains the error. This member is normally NO_ERROR, except when an EAPHost error occurs.

## -remarks

The <b>ONEX_STATUS</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

The <b>oneXStatus</b> member of the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure contains an <b>ONEX_STATUS</b> structure.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type">ONEX_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_reason_code">ONEX_REASON_CODE</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>