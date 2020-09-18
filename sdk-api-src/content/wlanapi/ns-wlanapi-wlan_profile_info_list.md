---
UID: NS:wlanapi._WLAN_PROFILE_INFO_LIST
title: WLAN_PROFILE_INFO_LIST (wlanapi.h)
description: Contains a list of wireless profile information.
helpviewer_keywords: ["*PWLAN_PROFILE_INFO_LIST","PWLAN_PROFILE_INFO_LIST","PWLAN_PROFILE_INFO_LIST structure pointer [NativeWIFI]","WLAN_PROFILE_INFO_LIST","WLAN_PROFILE_INFO_LIST structure [NativeWIFI]","nwifi.wlan_profile_info_list","wlanapi/PWLAN_PROFILE_INFO_LIST","wlanapi/WLAN_PROFILE_INFO_LIST"]
old-location: nwifi\wlan_profile_info_list.htm
tech.root: nwifi
ms.assetid: d5a3d475-0ae0-4860-a433-dd916c586f50
ms.date: 12/05/2018
ms.keywords: '*PWLAN_PROFILE_INFO_LIST, PWLAN_PROFILE_INFO_LIST, PWLAN_PROFILE_INFO_LIST structure pointer [NativeWIFI], WLAN_PROFILE_INFO_LIST, WLAN_PROFILE_INFO_LIST structure [NativeWIFI], nwifi.wlan_profile_info_list, wlanapi/PWLAN_PROFILE_INFO_LIST, wlanapi/WLAN_PROFILE_INFO_LIST'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
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
req.typenames: WLAN_PROFILE_INFO_LIST, *PWLAN_PROFILE_INFO_LIST
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_PROFILE_INFO_LIST
 - wlanapi/_WLAN_PROFILE_INFO_LIST
 - PWLAN_PROFILE_INFO_LIST
 - wlanapi/PWLAN_PROFILE_INFO_LIST
 - WLAN_PROFILE_INFO_LIST
 - wlanapi/WLAN_PROFILE_INFO_LIST
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
 - WLAN_PROFILE_INFO_LIST
---

# WLAN_PROFILE_INFO_LIST structure


## -description

The <b>WLAN_PROFILE_INFO_LIST</b> structure contains a list of wireless profile  information.

## -struct-fields

### -field dwNumberOfItems

The number of wireless profile entries in the <b>ProfileInfo</b> member.

### -field dwIndex

The index of the current item.  The index of the first item is 0. The <b>dwIndex</b> member must be less than the <b>dwNumberOfItems</b> member.

This member is not used by the wireless service. Applications can use this member when processing individual profiles in the   <b>WLAN_PROFILE_INFO_LIST</b> structure. When an application passes this structure from one function to another, it can set the value of <b>dwIndex</b> to the index of the item currently being processed. This can help an application maintain state.  

<b>dwIndex</b> should always be initialized before use.

### -field ProfileInfo.unique

### -field ProfileInfo.size_is

### -field ProfileInfo.size_is.dwNumberOfItems

### -field ProfileInfo

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info">WLAN_PROFILE_INFO</a> structures containing interface information. The number of items in the array is specified in the <b>dwNumberOfItems</b> member.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info">WLAN_PROFILE_INFO</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>