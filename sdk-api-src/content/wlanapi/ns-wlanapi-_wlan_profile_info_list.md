---
UID: NS:wlanapi._WLAN_PROFILE_INFO_LIST
title: "_WLAN_PROFILE_INFO_LIST"
author: windows-driver-content
description: Contains a list of wireless profile information.
old-location: nwifi\wlan_profile_info_list.htm
old-project: NativeWiFi
ms.assetid: d5a3d475-0ae0-4860-a433-dd916c586f50
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PWLAN_PROFILE_INFO_LIST, PWLAN_PROFILE_INFO_LIST, PWLAN_PROFILE_INFO_LIST structure pointer [NativeWIFI], WLAN_PROFILE_INFO_LIST, WLAN_PROFILE_INFO_LIST structure [NativeWIFI], _WLAN_PROFILE_INFO_LIST, nwifi.wlan_profile_info_list, wlanapi/PWLAN_PROFILE_INFO_LIST, wlanapi/WLAN_PROFILE_INFO_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WLAN_PROFILE_INFO_LIST, *PWLAN_PROFILE_INFO_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_PROFILE_INFO_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_PROFILE_INFO_LIST structure


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

An array of <a href="https://msdn.microsoft.com/ca45278c-2e1e-4080-825a-d6a05e463858">WLAN_PROFILE_INFO</a> structures containing interface information. The number of items in the array is specified in the <b>dwNumberOfItems</b> member.


## -see-also




<a href="https://msdn.microsoft.com/ca45278c-2e1e-4080-825a-d6a05e463858">WLAN_PROFILE_INFO</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>
 

 

