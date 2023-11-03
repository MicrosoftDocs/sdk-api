---
UID: NF:wlanapi.WlanSetProfile
title: WlanSetProfile function (wlanapi.h)
description: Sets the content of a specific profile.
helpviewer_keywords: ["WLAN_PROFILE_GROUP_POLICY","WLAN_PROFILE_USER","WlanSetProfile","WlanSetProfile function [NativeWIFI]","nwifi.wlansetprofile","wlanapi/WlanSetProfile"]
old-location: nwifi\wlansetprofile.htm
tech.root: nwifi
ms.assetid: 3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5
ms.date: 12/05/2018
ms.keywords: WLAN_PROFILE_GROUP_POLICY, WLAN_PROFILE_USER, WlanSetProfile, WlanSetProfile function [NativeWIFI], nwifi.wlansetprofile, wlanapi/WlanSetProfile
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
 - WlanSetProfile
 - wlanapi/WlanSetProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanSetProfile
---

# WlanSetProfile function


## -description

The <b>WlanSetProfile</b> function sets the content of a specific profile.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param dwFlags [in]

The flags to set on the profile.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><i>dwFlags</i> must be 0. Per-user profiles are not supported.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The profile is an all-user profile.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_GROUP_POLICY"></a><a id="wlan_profile_group_policy"></a><dl>
<dt><b>WLAN_PROFILE_GROUP_POLICY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The profile is a group policy profile.  

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_USER"></a><a id="wlan_profile_user"></a><dl>
<dt><b>WLAN_PROFILE_USER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The profile is a per-user profile.  

</td>
</tr>
</table>

### -param strProfileXml [in]

Contains the XML representation of the profile. The <a href="/windows/desktop/NativeWiFi/wlan-profileschema-wlanprofile-element">WLANProfile</a> element is the root profile element. To view sample profiles, see <a href="/windows/desktop/NativeWiFi/wireless-profile-samples">Wireless Profile Samples</a>. There is no predefined maximum string length.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The supplied profile must meet the compatibility criteria described in <a href="/windows/desktop/NativeWiFi/wireless-profile-compatibility">Wireless Profile Compatibility</a>.

### -param strAllUserProfileSecurity [in, optional]

Sets the security descriptor string on the all-user profile.  For more information about profile permissions, see the Remarks section.

If <i>dwFlags</i> is set to WLAN_PROFILE_USER, this parameter is ignored.

If this parameter is set to <b>NULL</b> for a new all-user profile, the security descriptor associated with the  wlan_secure_add_new_all_user_profiles object is used. If the security descriptor has not been modified by a <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a> call,  all users have default permissions on a new all-user profile. Call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings">WlanGetSecuritySettings</a> to get the default permissions associated with the   wlan_secure_add_new_all_user_profiles object.

If this parameter is set to <b>NULL</b> for an existing all-user profile, the permissions of the profile are not changed.

If this parameter is not <b>NULL</b> for an all-user profile, the security descriptor string associated with the profile is created or modified  after the security descriptor object is created and parsed as a string.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This parameter must be <b>NULL</b>.

### -param bOverwrite [in]

Specifies whether this profile is overwriting an existing profile.  If this parameter is <b>FALSE</b> and the profile already exists, the existing profile will not be overwritten and an error will be returned.

### -param pReserved [in]

Reserved for future use.  Must be set to <b>NULL</b>.

### -param pdwReasonCode [out]

A <a href="/windows/desktop/NativeWiFi/wlan-reason-code">WLAN_REASON_CODE</a> value that indicates why the profile is not valid.

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
The caller does not have sufficient permissions to set the profile.  

When called with <i>dwFlags</i> set to 0 - that is, when setting an all-user profile -  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>  retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_add_new_all_user_profiles</b> object. When called with <i>dwFlags</i> set to <b>WLAN_PROFILE_USER</b> - that is, when setting a per-user profile -  <b>WlanSetProfile</b>  retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_add_new_per_user_profiles</b> object. In either case, if the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanSetProfile</b> returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
<i>strProfileXml</i> specifies a network that already exists. Typically, this return value is used when <i>bOverwrite</i> is <b>FALSE</b>; however, if <i>bOverwrite</i> is <b>TRUE</b> and <i>dwFlags</i> specifies a different profile type than the one used by the existing profile,   then the existing profile will not be overwritten and <b>ERROR_ALREADY_EXISTS</b> will be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The profile specified by <i>strProfileXml</i> is not valid. If this value is returned, <i>pdwReasonCode</i> specifies the reason the profile is invalid.

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
<li><i>pReserved</i> is not <b>NULL</b>.</li>
<li><i>strProfileXml</i> is <b>NULL</b>.</li>
[ConfigBlob](/windows/desktop/eaphost/eaphostconfigschema-configblob-eaphostconfig-element). If the profile must have an empty <b>ConfigBlob</b>, use <code>&lt;ConfigBlob&gt;00&lt;/ConfigBlob&gt;</code> in the profile.</li>
<li><i>pdwReasonCode</i> is <b>NULL</b>.</li>
<li><i>dwFlags</i> is not set to one of the specified values.</li>
<li><i>dwFlags</i> is set to WLAN_PROFILE_GROUP_POLICY and <i>bOverwrite</i> is set to <b>FALSE</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
The interface does not support one or more of the capabilities specified in the profile. For example, if a profile specifies the use of WPA2 when the NIC only supports WPA, then this error code is returned. Also, if a profile specifies the use of FIPS mode when the NIC does not support FIPS mode, then this error code is returned.

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

The <b>WlanSetProfile</b> function can be used to add a new wireless LAN profile or replace an existing wireless LAN profile. 

A new profile is added at the top of the list after the group policy profiles.   A profile's position in the list is not changed if an existing profile is overwritten.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><p class="note">Ad hoc profiles appear after the infrastructure profiles in the profile list. If you create a new ad hoc profile, it is placed at the top of the ad hoc list, after the group policy and infrastructure profiles. 

<p class="note">802.1X guest profiles, Wireless Provisioning Service (WPS) profiles, and profiles with Wi-Fi Protected Access-None (WPA-None)  authentication are not supported. That means such a profile cannot be created, deleted, enumerated, or accessed using Native Wifi functions. Any such profile already in the preferred profile list will remain in the list, and its position in the list relative to other profiles is fixed unless the position of the other profiles change.





You can call <b>WlanSetProfile</b> on a profile that contains a plaintext key (that is, a profile with the  <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#protected">protected</a> element present and set to <b>FALSE</b>).  Before the profile is saved in the profile store, the key material is automatically encrypted. When the profile is subsequently retrieved from the profile store by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>, the encrypted key material is returned.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The key material is never encrypted.



All-user profiles have three associated permissions: read, write, and execute. If a user has read access, the user can view profile permissions. If a user has execute access, the user has read access and the user can also connect to and disconnect from a network using the profile. If a user has write access, the user has execute access and the user can also modify and delete permissions associated with a profile.

The following describes the procedure for creating a security descriptor object and parsing it as a string.

<ol>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a> to create a security descriptor in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a> to create a discretionary access control list (DACL) in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a> or <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a> to add access control entries (ACEs) to the DACL. Set the <i>AccessMask</i> parameter to one of the following as appropriate:<ul>
<li>WLAN_READ_ACCESS</li>
<li>WLAN_EXECUTE_ACCESS</li>
<li>WLAN_WRITE_ACCESS     </li>
</ul>
</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a> to add the DACL to the security descriptor.</li>
<li>Call <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> to convert the descriptor to string.</li>
</ol>
The string returned by <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> can then be used as the <i>strAllUserProfileSecurity</i> parameter value when calling <b>WlanSetProfile</b>.

For every wireless LAN profile used by the Native Wifi AutoConfig service, Windows maintains the concept of custom user data.  This custom user data is initially non-existent, but can be set by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a> function. The custom user data gets reset to empty any time the profile is modified by calling the <b>WlanSetProfile</b> function. Once custom user data has been set, this data can be accessed using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a> function. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfile</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example). 

The <b>netsh wlan add profile</b> command provides similar functionality at the command line. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>.

## -see-also

<a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a>