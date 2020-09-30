---
UID: NF:wlanapi.WlanSetProfilePosition
title: WlanSetProfilePosition function (wlanapi.h)
description: Sets the position of a single, specified profile in the preference list.
helpviewer_keywords: ["WlanSetProfilePosition","WlanSetProfilePosition function [NativeWIFI]","nwifi.wlansetprofileposition","wlanapi/WlanSetProfilePosition"]
old-location: nwifi\wlansetprofileposition.htm
tech.root: nwifi
ms.assetid: 06ef9f55-b425-4f61-9b9e-3c27cc3796f6
ms.date: 12/05/2018
ms.keywords: WlanSetProfilePosition, WlanSetProfilePosition function [NativeWIFI], nwifi.wlansetprofileposition, wlanapi/WlanSetProfilePosition
req.header: wlanapi.h
req.include-header: Wlanapi.h
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanSetProfilePosition
 - wlanapi/WlanSetProfilePosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanSetProfilePosition
---

# WlanSetProfilePosition function


## -description

The <b>WlanSetProfilePosition</b> function sets the position of a single, specified profile in the preference list.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param strProfileName [in]

The name of the profile. Profile names are case-sensitive. This string must be NULL-terminated.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The supplied name must match the profile name derived automatically from the SSID of the network. For an infrastructure network profile, the SSID must be supplied for the profile name. For an ad hoc network profile, the supplied name must be the SSID of the ad hoc network followed by <code>-adhoc</code>.

### -param dwPosition [in]

Indicates the position in the preference list that the profile should be shifted to.  0 (zero) corresponds to the first profile in the list that is returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a> function.

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions to change the profile position.  

Before <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a> performs an operation that changes the relative order of all-user profiles in the profile list  or moves an all-user profile to a lower position in the profile list,  <b>WlanSetProfilePosition</b>  retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_all_user_profiles_order</b> object. If the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanSetProfilePosition</b>  returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid,  <i>pInterfaceGuid</i> is <b>NULL</b>, <i>strProfileName</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>

## -remarks

The position of group policy profiles cannot be changed.

By default, only a user logged on as a member of the Administrators group can change the position of an all-user profile. Call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings">WlanGetSecuritySettings</a> to determine the actual user rights required to change the position of an all-user profile.

To set the profile position at the command line, use the <b>netsh wlan set profileorder</b> command. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>. 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Ad hoc profiles appear after the infrastructure profiles in the profile list. If you try to position an ad hoc profile before an infrastructure profile using <b>WlanSetProfilePosition</b>, the   <b>WlanSetProfilePosition</b> call will succeed but the Wireless Zero Configuration service will reorder the profile list such that the ad hoc profile is positioned after all infrastructure network profiles.

Guest profiles, profiles with Wireless Provisioning Service (WPS) authentication, and profiles with Wi-Fi Protected Access-None (WPA-None)  authentication are not supported. Any such profile that appears in the preferred profile list has a fixed position in the profile list. That means its position cannot be changed using <b>WlanSetProfilePosition</b> and that its position is not affected by position changes of other profiles. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfilePosition</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example).

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a>