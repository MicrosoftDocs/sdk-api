---
UID: NS:dot1x._ONEX_VARIABLE_BLOB
title: ONEX_VARIABLE_BLOB (dot1x.h)
description: Is used as a member of other 802.1X authentication structures to contain variable-sized members.
helpviewer_keywords: ["*PONEX_VARIABLE_BLOB","ONEX_VARIABLE_BLOB","ONEX_VARIABLE_BLOB structure [NativeWIFI]","PONEX_VARIABLE_BLOB","PONEX_VARIABLE_BLOB structure pointer [NativeWIFI]","dot1x/ONEX_VARIABLE_BLOB","dot1x/PONEX_VARIABLE_BLOB","nwifi.onex_variable_blob"]
old-location: nwifi\onex_variable_blob.htm
tech.root: nwifi
ms.assetid: 3a410bde-bcff-4a86-aadc-650862dbf38b
ms.date: 12/05/2018
ms.keywords: '*PONEX_VARIABLE_BLOB, ONEX_VARIABLE_BLOB, ONEX_VARIABLE_BLOB structure [NativeWIFI], PONEX_VARIABLE_BLOB, PONEX_VARIABLE_BLOB structure pointer [NativeWIFI], dot1x/ONEX_VARIABLE_BLOB, dot1x/PONEX_VARIABLE_BLOB, nwifi.onex_variable_blob'
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
req.typenames: ONEX_VARIABLE_BLOB, *PONEX_VARIABLE_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ONEX_VARIABLE_BLOB
 - dot1x/_ONEX_VARIABLE_BLOB
 - PONEX_VARIABLE_BLOB
 - dot1x/PONEX_VARIABLE_BLOB
 - ONEX_VARIABLE_BLOB
 - dot1x/ONEX_VARIABLE_BLOB
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
 - ONEX_VARIABLE_BLOB
---

# ONEX_VARIABLE_BLOB structure


## -description

The <b>ONEX_VARIABLE_BLOB</b> structure is used as a member of other 802.1X authentication structures to contain variable-sized members.

## -struct-fields

### -field dwSize

The size, in bytes, of this <b>ONEX_VARIABLE_BLOB</b> structure.

### -field dwOffset

The offset, in bytes, from the beginning of the containing outer structure (where the <b>ONEX_VARIABLE_BLOB</b> structure is a  member) to the data contained in the <b>ONEX_VARIABLE_BLOB</b> structure.

## -remarks

The <b>ONEX_VARIABLE_BLOB</b> structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and  later.  

The <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> contains information on a status change to 802.1X authentication. The <b>ONEX_RESULT_UPDATE_DATA</b> structure is returned  when  the <b>NotificationSource</b> member of the <a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a> structure is <b>WLAN_NOTIFICATION_SOURCE_ONEX</b>  and the <b>NotificationCode</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure for received notification  is <b>OneXNotificationTypeResultUpdate</b>. For this notification, the <b>pData</b> member of the <b>WLAN_NOTIFICATION_DATA</b> structure points to an  <b>ONEX_RESULT_UPDATE_DATA</b> structure that contains information on the 802.1X authentication status change. 

A number of the nested structure members in the <a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a> structure contains members of the <b>ONEX_VARIABLE_BLOB</b> type.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-acm-architecture">About the ACM Architecture</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params">ONEX_AUTH_PARAMS</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_eap_error">ONEX_EAP_ERROR</a>



<a href="/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type">ONEX_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data">ONEX_RESULT_UPDATE_DATA</a>



<a href="/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)">WLAN_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>