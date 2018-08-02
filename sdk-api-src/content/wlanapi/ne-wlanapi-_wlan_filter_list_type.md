---
UID: NE:wlanapi._WLAN_FILTER_LIST_TYPE
title: "_WLAN_FILTER_LIST_TYPE"
author: windows-sdk-content
description: Indicates types of filter lists.
old-location: nwifi\wlan_filter_list_type.htm
old-project: NativeWiFi
ms.assetid: b53b9a6c-6453-4828-9662-589a1b99614c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWLAN_FILTER_LIST_TYPE, PWLAN_FILTER_LIST_TYPE, PWLAN_FILTER_LIST_TYPE enumeration pointer [NativeWIFI], WLAN_FILTER_LIST_TYPE, WLAN_FILTER_LIST_TYPE enumeration [NativeWIFI], _WLAN_FILTER_LIST_TYPE, nwifi.wlan_filter_list_type, wlan_filter_list_type_gp_deny, wlan_filter_list_type_gp_permit, wlan_filter_list_type_user_deny, wlan_filter_list_type_user_permit, wlanapi/PWLAN_FILTER_LIST_TYPE, wlanapi/WLAN_FILTER_LIST_TYPE, wlanapi/wlan_filter_list_type_gp_deny, wlanapi/wlan_filter_list_type_gp_permit, wlanapi/wlan_filter_list_type_user_deny, wlanapi/wlan_filter_list_type_user_permit"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WLAN_FILTER_LIST_TYPE, *PWLAN_FILTER_LIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_FILTER_LIST_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_FILTER_LIST_TYPE enumeration


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




<a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a>



<a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a>
 

 

