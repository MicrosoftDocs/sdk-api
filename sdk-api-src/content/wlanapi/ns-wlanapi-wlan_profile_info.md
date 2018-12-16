---
UID: NS:wlanapi._WLAN_PROFILE_INFO
title: WLAN_PROFILE_INFO
author: windows-sdk-content
description: Basic information about a profile.
old-location: nwifi\wlan_profile_info.htm
tech.root: NativeWiFi
ms.assetid: ca45278c-2e1e-4080-825a-d6a05e463858
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_PROFILE_INFO, PWLAN_PROFILE_INFO, PWLAN_PROFILE_INFO structure pointer [NativeWIFI], WLAN_PROFILE_GROUP_POLICY, WLAN_PROFILE_INFO, WLAN_PROFILE_INFO structure [NativeWIFI], WLAN_PROFILE_USER, nwifi.wlan_profile_info, wlanapi/PWLAN_PROFILE_INFO, wlanapi/WLAN_PROFILE_INFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_PROFILE_INFO
product: Windows
targetos: Windows
req.typenames: WLAN_PROFILE_INFO, *PWLAN_PROFILE_INFO
req.redist: Wireless LAN API for Windows XP with SP2
---

# WLAN_PROFILE_INFO structure


## -description


The <b>WLAN_PROFILE_INFO</b> structure contains basic information about a profile.


## -struct-fields




### -field strProfileName

The name of the profile.  This value may be the name of a domain if the profile is for provisioning. Profile names are case-sensitive. This string must be NULL-terminated.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The name of the profile is derived automatically from the SSID of the wireless network. For infrastructure network profiles, the name of the profile is the SSID of the network. For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by <code>-adhoc</code>.


### -field dwFlags

A set of flags specifying settings for wireless profile. These values are defined in the <i>Wlanapi.h</i> header file. 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><i>dwFlags</i> must be 0. Per-user profiles are not supported.


Combinations of these flag bits are possible



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_GROUP_POLICY"></a><a id="wlan_profile_group_policy"></a><dl>
<dt><b>WLAN_PROFILE_GROUP_POLICY</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates that this profile was created by group policy.  A group policy profile is read-only. Neither the content nor the preference order of the profile can be changed.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_USER"></a><a id="wlan_profile_user"></a><dl>
<dt><b>WLAN_PROFILE_USER</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates that the profile is a per-user profile.  If not set, this profile is an all-user profile.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/d5a3d475-0ae0-4860-a433-dd916c586f50">WLAN_PROFILE_INFO_LIST</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>
 

 

