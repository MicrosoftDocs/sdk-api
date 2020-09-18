---
UID: NE:wlanapi._WLAN_FILTER_LIST_TYPE
title: WLAN_FILTER_LIST_TYPE (wlanapi.h)
description: Indicates types of filter lists.
helpviewer_keywords: ["*PWLAN_FILTER_LIST_TYPE","PWLAN_FILTER_LIST_TYPE","PWLAN_FILTER_LIST_TYPE enumeration pointer [NativeWIFI]","WLAN_FILTER_LIST_TYPE","WLAN_FILTER_LIST_TYPE enumeration [NativeWIFI]","nwifi.wlan_filter_list_type","wlan_filter_list_type_gp_deny","wlan_filter_list_type_gp_permit","wlan_filter_list_type_user_deny","wlan_filter_list_type_user_permit","wlanapi/PWLAN_FILTER_LIST_TYPE","wlanapi/WLAN_FILTER_LIST_TYPE","wlanapi/wlan_filter_list_type_gp_deny","wlanapi/wlan_filter_list_type_gp_permit","wlanapi/wlan_filter_list_type_user_deny","wlanapi/wlan_filter_list_type_user_permit"]
old-location: nwifi\wlan_filter_list_type.htm
tech.root: nwifi
ms.assetid: b53b9a6c-6453-4828-9662-589a1b99614c
ms.date: 12/05/2018
ms.keywords: '*PWLAN_FILTER_LIST_TYPE, PWLAN_FILTER_LIST_TYPE, PWLAN_FILTER_LIST_TYPE enumeration pointer [NativeWIFI], WLAN_FILTER_LIST_TYPE, WLAN_FILTER_LIST_TYPE enumeration [NativeWIFI], nwifi.wlan_filter_list_type, wlan_filter_list_type_gp_deny, wlan_filter_list_type_gp_permit, wlan_filter_list_type_user_deny, wlan_filter_list_type_user_permit, wlanapi/PWLAN_FILTER_LIST_TYPE, wlanapi/WLAN_FILTER_LIST_TYPE, wlanapi/wlan_filter_list_type_gp_deny, wlanapi/wlan_filter_list_type_gp_permit, wlanapi/wlan_filter_list_type_user_deny, wlanapi/wlan_filter_list_type_user_permit'
req.header: wlanapi.h
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
req.typenames: WLAN_FILTER_LIST_TYPE, *PWLAN_FILTER_LIST_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_FILTER_LIST_TYPE
 - wlanapi/_WLAN_FILTER_LIST_TYPE
 - PWLAN_FILTER_LIST_TYPE
 - wlanapi/PWLAN_FILTER_LIST_TYPE
 - WLAN_FILTER_LIST_TYPE
 - wlanapi/WLAN_FILTER_LIST_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_FILTER_LIST_TYPE
---

# WLAN_FILTER_LIST_TYPE enumeration


## -description

The <b>WLAN_FILTER_LIST_TYPE</b> enumerated type indicates types of filter lists.

## -enum-fields

### -field wlan_filter_list_type_gp_permit

Group policy permit list.

### -field wlan_filter_list_type_gp_deny

Group policy deny list.

### -field wlan_filter_list_type_user_permit

User permit list.

### -field wlan_filter_list_type_user_deny

User deny list.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>