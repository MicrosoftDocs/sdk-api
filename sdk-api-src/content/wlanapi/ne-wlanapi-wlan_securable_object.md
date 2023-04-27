---
UID: NE:wlanapi._WLAN_SECURABLE_OBJECT
title: WLAN_SECURABLE_OBJECT (wlanapi.h)
description: Defines the securable objects used by Native Wifi Functions.
helpviewer_keywords: ["*PWLAN_SECURABLE_OBJECT","PWLAN_SECURABLE_OBJECT","PWLAN_SECURABLE_OBJECT enumeration pointer [NativeWIFI]","WLAN_SECURABLE_OBJECT","WLAN_SECURABLE_OBJECT enumeration [NativeWIFI]","nwifi.wlan_securable_object","wlan_secure_ac_enabled","wlan_secure_add_new_all_user_profiles","wlan_secure_add_new_per_user_profiles","wlan_secure_all_user_profiles_order","wlan_secure_bc_scan_enabled","wlan_secure_bss_type","wlan_secure_current_operation_mode","wlan_secure_deny_list","wlan_secure_get_plaintext_key","wlan_secure_hosted_network_elevated_access","wlan_secure_ihv_control","wlan_secure_interface_properties","wlan_secure_media_streaming_mode_enabled","wlan_secure_permit_list","wlan_secure_show_denied","wlan_secure_virtual_station_extensibility","wlan_secure_wfd_elevated_access","wlanapi/PWLAN_SECURABLE_OBJECT","wlanapi/WLAN_SECURABLE_OBJECT","wlanapi/wlan_secure_ac_enabled","wlanapi/wlan_secure_add_new_all_user_profiles","wlanapi/wlan_secure_add_new_per_user_profiles","wlanapi/wlan_secure_all_user_profiles_order","wlanapi/wlan_secure_bc_scan_enabled","wlanapi/wlan_secure_bss_type","wlanapi/wlan_secure_current_operation_mode","wlanapi/wlan_secure_deny_list","wlanapi/wlan_secure_get_plaintext_key","wlanapi/wlan_secure_hosted_network_elevated_access","wlanapi/wlan_secure_ihv_control","wlanapi/wlan_secure_interface_properties","wlanapi/wlan_secure_media_streaming_mode_enabled","wlanapi/wlan_secure_permit_list","wlanapi/wlan_secure_show_denied","wlanapi/wlan_secure_virtual_station_extensibility","wlanapi/wlan_secure_wfd_elevated_access"]
old-location: nwifi\wlan_securable_object.htm
tech.root: nwifi
ms.assetid: 1f6e1460-d27f-4800-8a32-6f9f509753cf
ms.date: 12/05/2018
ms.keywords: '*PWLAN_SECURABLE_OBJECT, PWLAN_SECURABLE_OBJECT, PWLAN_SECURABLE_OBJECT enumeration pointer [NativeWIFI], WLAN_SECURABLE_OBJECT, WLAN_SECURABLE_OBJECT enumeration [NativeWIFI], nwifi.wlan_securable_object, wlan_secure_ac_enabled, wlan_secure_add_new_all_user_profiles, wlan_secure_add_new_per_user_profiles, wlan_secure_all_user_profiles_order, wlan_secure_bc_scan_enabled, wlan_secure_bss_type, wlan_secure_current_operation_mode, wlan_secure_deny_list, wlan_secure_get_plaintext_key, wlan_secure_hosted_network_elevated_access, wlan_secure_ihv_control, wlan_secure_interface_properties, wlan_secure_media_streaming_mode_enabled, wlan_secure_permit_list, wlan_secure_show_denied, wlan_secure_virtual_station_extensibility, wlan_secure_wfd_elevated_access, wlanapi/PWLAN_SECURABLE_OBJECT, wlanapi/WLAN_SECURABLE_OBJECT, wlanapi/wlan_secure_ac_enabled, wlanapi/wlan_secure_add_new_all_user_profiles, wlanapi/wlan_secure_add_new_per_user_profiles, wlanapi/wlan_secure_all_user_profiles_order, wlanapi/wlan_secure_bc_scan_enabled, wlanapi/wlan_secure_bss_type, wlanapi/wlan_secure_current_operation_mode, wlanapi/wlan_secure_deny_list, wlanapi/wlan_secure_get_plaintext_key, wlanapi/wlan_secure_hosted_network_elevated_access, wlanapi/wlan_secure_ihv_control, wlanapi/wlan_secure_interface_properties, wlanapi/wlan_secure_media_streaming_mode_enabled, wlanapi/wlan_secure_permit_list, wlanapi/wlan_secure_show_denied, wlanapi/wlan_secure_virtual_station_extensibility, wlanapi/wlan_secure_wfd_elevated_access'
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
req.typenames: WLAN_SECURABLE_OBJECT, *PWLAN_SECURABLE_OBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_SECURABLE_OBJECT
 - wlanapi/_WLAN_SECURABLE_OBJECT
 - PWLAN_SECURABLE_OBJECT
 - wlanapi/PWLAN_SECURABLE_OBJECT
 - WLAN_SECURABLE_OBJECT
 - wlanapi/WLAN_SECURABLE_OBJECT
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
 - WLAN_SECURABLE_OBJECT
---

# WLAN_SECURABLE_OBJECT enumeration


## -description

The <b>WLAN_SECURABLE_OBJECT</b> enumerated type defines the <a href="/windows/desktop/SecAuthZ/securable-objects">securable objects</a> used by <a href="/windows/desktop/NativeWiFi/native-wifi-functions">Native Wifi Functions</a>.

These objects can be secured using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a>. The current permissions associated with these objects can be retrieved using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings">WlanGetSecuritySettings</a>. For more information about the use of securable objects, see <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How DACLs Control Access to an Object</a>.

## -enum-fields

### -field wlan_secure_permit_list:0

The permissions for modifying the permit list for user profiles.

The <a href="/windows/desktop/SecAuthZ/access-control-lists">discretionary access control lists (DACL)</a> associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a> is called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_permit</b>. For the <b>WlanGetFilterList</b> call to succeed, the DACL must contain an <a href="/windows/desktop/SecAuthZ/access-control-entries">access control entry (ACE)</a> that grants WLAN_READ_ACCESS permission to the <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> of the calling thread. For the  <b>WlanSetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_deny_list

The permissions for modifying the deny list for user profiles. The auto config service will not establish a connection to a network on the deny list.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a> is called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_deny</b>. For the <b>WlanGetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_ac_enabled

The permissions for enabling  the auto config service.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_autoconf_enabled</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_bc_scan_enabled

The permissions for enabling background scans.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_background_scan_enabled</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_bss_type

The permissions for altering the basic service set type.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_bss_type</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_show_denied

  The permissions  for modifying whether networks on the deny list appear in the available networks list.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetautoconfigparameter">WlanSetAutoConfigParameter</a> is called with <i>OpCode</i> set to <b>wlan_autoconf_opcode_show_denied_networks</b>. For the <b>WlanQueryAutoConfigParameter</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetAutoConfigParameter</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_interface_properties

The permissions for changing interface properties.

This is the generic securable object used by <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> when another more specific securable object is not used. Its DACL is retrieved whenever <b>WlanQueryInterface</b> or <b>WlanSetInterface</b> is access token of the calling thread and the <i>OpCode</i> is set to a value other than <b>wlan_intf_opcode_autoconf_enabled</b>, <b>wlan_intf_opcode_background_scan_enabled</b>, <b>wlan_intf_opcode_media_streaming_mode</b>, <b>wlan_intf_opcode_bss_type</b>, or <b>wlan_intf_opcode_current_operation_mode</b>. The DACL is also not retrieved when <i>OpCode</i> is set to <b>wlan_intf_opcode_radio_state</b> and the caller is the console user.

For the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_ihv_control

The permissions for using the  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol">WlanIhvControl</a> function for independent hardware vendor (IHV) control of WLAN drivers or services.

The DACL associated with this securable object is retrieved when <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol">WlanIhvControl</a>  is called. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_all_user_profiles_order

The permissions for modifying the order of all-user profiles.

The DACL associated with this securable object is retrieved before  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a> performs an operation that changes the relative order of all-user profiles in the profile list  or moves an all-user profile to a lower position in the profile list. For either call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_add_new_all_user_profiles

The permissions for adding new all-user profiles.

<div class="alert"><b>Note</b>  The security descriptor associated with this object is applied to new all-user profiles created.</div>
<div> </div>
The DACL associated with this securable object is retrieved when <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>  is called with <i>dwFlags</i> set to 0. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_add_new_per_user_profiles

The permissions for adding new per-user profiles.

The DACL associated with this securable object is retrieved when <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>  is called with <i>dwFlags</i> set to WLAN_PROFILE_USER. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_media_streaming_mode_enabled

The permissions for setting or querying the media streaming mode.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_media_streaming_mode</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_current_operation_mode

The permissions for setting or querying the operation mode of the wireless interface.

The DACL associated with this securable object is retrieved when either <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_current_operation_mode</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.

### -field wlan_secure_get_plaintext_key

The permissions for retrieving the plain text key from a wireless profile.

 The DACL associated with this securable object is retrieved when the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a> function is called with the <b>WLAN_PROFILE_GET_PLAINTEXT_KEY</b>  flag set in the value pointed to by the <i>pdwFlags</i> parameter on input. For the <b>WlanGetProfile</b> call to succeed, the DACL must contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local computer.



<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.

### -field wlan_secure_hosted_network_elevated_access

The permissions that have elevated access to call the privileged Hosted Network functions.  

The DACL associated with this securable object is retrieved when the  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a> function is called with the <i>OpCode</i> parameter set to <b>wlan_hosted_network_opcode_enable</b>. For the <b>WlanHostedNetworkSetProperty</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread. By default,  the permission to set the wireless Hosted Network property to <b>wlan_hosted_network_opcode_enable</b> is allowed only to the members of the Administrators group on a local computer.



 The DACL associated with this securable object is retrieved when the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestart">WlanHostedNetworkForceStart</a> function is called. For the <b>WlanHostedNetworkForceStart</b> call to succeed, the DACL must contain an ACE that grants <b>WLAN_WRITE_ACCESS</b> permission to the access token of the calling thread. By default,  the permission to force start the wireless Hosted Network is allowed only to the members of the Administrators group on a local computer.



<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.

### -field wlan_secure_virtual_station_extensibility

<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.

### -field wlan_secure_wfd_elevated_access

This value is reserved for internal use by the Wi-Fi Direct service.  

<b>Windows 8:  </b>This value is an extension to native wireless APIs added on Windows 8 and  later.

### -field WLAN_SECURABLE_OBJECT_COUNT

## -remarks

These objects can be secured using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a>. The current permissions associated with these objects can be retrieved using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings">WlanGetSecuritySettings</a>. For more information about the use of securable objects, see <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How DACLs Control Access to an Object</a> and <a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How DACLs Control Access to an Object</a>



<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestart">WlanHostedNetworkForceStart</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol">WlanIhvControl</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetautoconfigparameter">WlanSetAutoConfigParameter</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>



<b>WlanSetInterface</b>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a>
