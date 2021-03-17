---
UID: NF:wlanapi.WlanSaveTemporaryProfile
title: WlanSaveTemporaryProfile function (wlanapi.h)
description: Saves a temporary profile to the profile store.
helpviewer_keywords: ["WLAN_PROFILE_CONNECTION_MODE_AUTO","WLAN_PROFILE_CONNECTION_MODE_SET_BY_CLIENT","WLAN_PROFILE_USER","WlanSaveTemporaryProfile","WlanSaveTemporaryProfile function [NativeWIFI]","nwifi.wlansavetemporaryprofile","wlanapi/WlanSaveTemporaryProfile"]
old-location: nwifi\wlansavetemporaryprofile.htm
tech.root: nwifi
ms.assetid: e409fd30-eddd-4cc7-acb7-35af6ef51a10
ms.date: 12/05/2018
ms.keywords: WLAN_PROFILE_CONNECTION_MODE_AUTO, WLAN_PROFILE_CONNECTION_MODE_SET_BY_CLIENT, WLAN_PROFILE_USER, WlanSaveTemporaryProfile, WlanSaveTemporaryProfile function [NativeWIFI], nwifi.wlansavetemporaryprofile, wlanapi/WlanSaveTemporaryProfile
req.header: wlanapi.h
req.include-header: Wlanapi.h
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlanSaveTemporaryProfile
 - wlanapi/WlanSaveTemporaryProfile
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
 - WlanSaveTemporaryProfile
---

# WlanSaveTemporaryProfile function


## -description

The <b>WlanSaveTemporaryProfile</b> function saves a temporary profile to the profile store.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param strProfileName [in]

The name of the profile to be saved. Profile names are case-sensitive. This string must be NULL-terminated.

### -param strAllUserProfileSecurity [in, optional]

Sets the security descriptor string on the all-user profile.  By default, for a new all-user profile, all users have write access on the profile. For more information about profile permissions, see the Remarks section.

If <i>dwFlags</i> is set to WLAN_PROFILE_USER, this parameter is ignored.

If this parameter is set to <b>NULL</b> for an all-user profile, the default permissions are used.

If this parameter is not <b>NULL</b> for an all-user profile, the security descriptor string associated with the profile is created or modified  after the security descriptor object is created and parsed as a string.

### -param dwFlags [in]

Specifies the flags to set on the profile. The flags can be combined.

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
<td width="40%"><a id="WLAN_PROFILE_USER"></a><a id="wlan_profile_user"></a><dl>
<dt><b>WLAN_PROFILE_USER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The profile is a per-user profile.  

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_CONNECTION_MODE_SET_BY_CLIENT"></a><a id="wlan_profile_connection_mode_set_by_client"></a><dl>
<dt><b>WLAN_PROFILE_CONNECTION_MODE_SET_BY_CLIENT</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The profile was created by the client.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_CONNECTION_MODE_AUTO"></a><a id="wlan_profile_connection_mode_auto"></a><dl>
<dt><b>WLAN_PROFILE_CONNECTION_MODE_AUTO</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The profile was created by the automatic configuration module.

</td>
</tr>
</table>

### -param bOverWrite [in]

Specifies whether this profile is overwriting an existing profile.  If this parameter is <b>FALSE</b> and the profile already exists, the existing profile will not be overwritten and an error will be returned.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following conditions occurred:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b> or invalid.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
<li><i>dwFlags</i> is not set to a combination of one or more  of the values specified in the table above.</li>
<li><i>dwFlags</i> is set to WLAN_PROFILE_CONNECTION_MODE_AUTO and <i>strProfileName</i> is <b>NULL</b>.</li>
</ul>
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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value will be returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The interface is not currently connected using a temporary profile.

</td>
</tr>
</table>

## -remarks

A temporary profile is the one passed to <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a> or generated by the discovery engine.  A network connection can be established using a temporary profile.  Using this API saves the temporary profile and associated user data to the profile store.

A new profile is added at the top of the list after the group policy profiles. A profile's position in the list is not changed if an existing profile is overwritten.

All-user profiles have three associated permissions: read, write, and execute. If a user has read access, the user can view profile permissions. If a user has execute access, the user has read access and the user can also connect to and disconnect from a network using the profile. If a user has write access, the user has execute access and the user can also modify and delete permissions associated with a profile.

The following describes the procedure for creating a security descriptor object and parsing it as a string.

<ol>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a> to create a security descriptor in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a> to create a discretionary access control list (DACL) in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a> or <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a> to add access control entries (ACEs) to the DACL. Set the <i>AccessMask</i> parameter to one of the following bitwise OR combinations as appropriate:<ul>
<li>WLAN_READ_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS | WLAN_WRITE_ACCESS     </li>
</ul>
</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a> to add the DACL to the security descriptor.</li>
<li>Call <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> to convert the descriptor to string.</li>
</ol>
The string returned by <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> can then be used as the <i>strAllUserProfileSecurity</i> parameter value when calling <b>WlanSaveTemporaryProfile</b>.

## -see-also

<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>