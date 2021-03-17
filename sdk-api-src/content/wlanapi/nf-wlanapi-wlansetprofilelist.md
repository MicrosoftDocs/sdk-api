---
UID: NF:wlanapi.WlanSetProfileList
title: WlanSetProfileList function (wlanapi.h)
description: Sets the preference order of profiles.
helpviewer_keywords: ["WlanSetProfileList","WlanSetProfileList function [NativeWIFI]","nwifi.wlansetprofilelist","wlanapi/WlanSetProfileList"]
old-location: nwifi\wlansetprofilelist.htm
tech.root: nwifi
ms.assetid: 980c7920-a25e-4e05-a742-77178a7f000a
ms.date: 12/05/2018
ms.keywords: WlanSetProfileList, WlanSetProfileList function [NativeWIFI], nwifi.wlansetprofilelist, wlanapi/WlanSetProfileList
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
 - WlanSetProfileList
 - wlanapi/WlanSetProfileList
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
 - WlanSetProfileList
---

# WlanSetProfileList function


## -description

The <b>WlanSetProfileList</b> function sets the preference order of profiles for a given interface.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param dwItems [in]

The number of profiles in the <i>strProfileNames</i> parameter.

### -param strProfileNames [in]

The names of the profiles in the desired order. Profile names are case-sensitive. This string must be NULL-terminated.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The supplied names must match the profile names derived automatically from the SSID of the network. For infrastructure network profiles, the SSID must be supplied for the profile name. For ad hoc network profiles, the supplied name must be the SSID of the ad hoc network followed by <code>-adhoc</code>.

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
The caller does not have sufficient permissions to change the profile list.  

Before <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a> performs an operation that changes the relative order of all-user profiles in the profile list  or moves an all-user profile to a lower position in the profile list,  <b>WlanSetProfileList</b> retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_all_user_profiles_order</b> object. If the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanSetProfileList</b> returns <b>ERROR_ACCESS_DENIED</b>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following conditions occurred:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b> or invalid.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>dwItems</i> is 0.</li>
<li><i>strProfileNames</i> is <b>NULL</b>.</li>
<li>The same profile name appears more than once in <i>strProfileNames</i>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
<i>strProfileNames</i> contains the name of a profile that is not present in the profile store.

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

The <b>WlanSetProfileList</b> function sets the preference order of wireless LAN profiles for a given wireless interface.

The profiles in the list must be a one-to-one match with the current profiles returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a> function.  The position of group policy profiles cannot be changed.

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfileList</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example).

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>