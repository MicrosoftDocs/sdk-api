---
UID: NE:wlanapi._WLAN_SECURABLE_OBJECT
title: "_WLAN_SECURABLE_OBJECT"
author: windows-sdk-content
description: Defines the securable objects used by Native Wifi Functions.
old-location: nwifi\wlan_securable_object.htm
old-project: NativeWiFi
ms.assetid: 1f6e1460-d27f-4800-8a32-6f9f509753cf
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PWLAN_SECURABLE_OBJECT, PWLAN_SECURABLE_OBJECT, PWLAN_SECURABLE_OBJECT enumeration pointer [NativeWIFI], WLAN_SECURABLE_OBJECT, WLAN_SECURABLE_OBJECT enumeration [NativeWIFI], _WLAN_SECURABLE_OBJECT, nwifi.wlan_securable_object, wlan_secure_ac_enabled, wlan_secure_add_new_all_user_profiles, wlan_secure_add_new_per_user_profiles, wlan_secure_all_user_profiles_order, wlan_secure_bc_scan_enabled, wlan_secure_bss_type, wlan_secure_current_operation_mode, wlan_secure_deny_list, wlan_secure_get_plaintext_key, wlan_secure_hosted_network_elevated_access, wlan_secure_ihv_control, wlan_secure_interface_properties, wlan_secure_media_streaming_mode_enabled, wlan_secure_permit_list, wlan_secure_show_denied, wlan_secure_virtual_station_extensibility, wlan_secure_wfd_elevated_access, wlanapi/PWLAN_SECURABLE_OBJECT, wlanapi/WLAN_SECURABLE_OBJECT, wlanapi/wlan_secure_ac_enabled, wlanapi/wlan_secure_add_new_all_user_profiles, wlanapi/wlan_secure_add_new_per_user_profiles, wlanapi/wlan_secure_all_user_profiles_order, wlanapi/wlan_secure_bc_scan_enabled, wlanapi/wlan_secure_bss_type, wlanapi/wlan_secure_current_operation_mode, wlanapi/wlan_secure_deny_list, wlanapi/wlan_secure_get_plaintext_key, wlanapi/wlan_secure_hosted_network_elevated_access, wlanapi/wlan_secure_ihv_control, wlanapi/wlan_secure_interface_properties, wlanapi/wlan_secure_media_streaming_mode_enabled, wlanapi/wlan_secure_permit_list, wlanapi/wlan_secure_show_denied, wlanapi/wlan_secure_virtual_station_extensibility, wlanapi/wlan_secure_wfd_elevated_access"
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
req.typenames: WLAN_SECURABLE_OBJECT, *PWLAN_SECURABLE_OBJECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_SECURABLE_OBJECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_SECURABLE_OBJECT enumeration


## -description


The <b>WLAN_SECURABLE_OBJECT</b> enumerated type defines the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable objects</a> used by <a href="https://msdn.microsoft.com/c1816d68-48b2-4d3d-a8c8-4a243a4b3f3b">Native Wifi Functions</a>.

These objects can be secured using <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a>. The current permissions associated with these objects can be retrieved using <a href="https://msdn.microsoft.com/5e14a70c-c049-4cd1-8675-2b01ed11463f">WlanGetSecuritySettings</a>. For more information about the use of securable objects, see <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How DACLs Control Access to an Object</a>.


## -enum-fields




### -field wlan_secure_permit_list

The permissions for modifying the permit list for user profiles.

The <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">discretionary access control lists (DACL)</a> associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a> or <a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a> is called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_permit</b>. For the <b>WlanGetFilterList</b> call to succeed, the DACL must contain an <a href="https://msdn.microsoft.com/9cf4d796-3955-456b-9db9-ae9fa83752f6">access control entry (ACE)</a> that grants WLAN_READ_ACCESS permission to the <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a> of the calling thread. For the  <b>WlanSetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_deny_list

The permissions for modifying the deny list for user profiles. The auto config service will not establish a connection to a network on the deny list.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a> or <a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a> is called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_deny</b>. For the <b>WlanGetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetFilterList</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_ac_enabled

The permissions for enabling  the auto config service.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_autoconf_enabled</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_bc_scan_enabled

The permissions for enabling background scans.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_background_scan_enabled</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_bss_type

The permissions for altering the basic service set type.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_bss_type</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_show_denied

  The permissions  for modifying whether networks on the deny list appear in the available networks list.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a> or <a href="https://msdn.microsoft.com/4f2514be-f05e-4be6-8c74-ef7a9ffe1c53">WlanSetAutoConfigParameter</a> is called with <i>OpCode</i> set to <b>wlan_autoconf_opcode_show_denied_networks</b>. For the <b>WlanQueryAutoConfigParameter</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetAutoConfigParameter</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_interface_properties

The permissions for changing interface properties.

This is the generic securable object used by <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> when another more specific securable object is not used. Its DACL is retrieved whenever <b>WlanQueryInterface</b> or <b>WlanSetInterface</b> is access token of the calling thread and the <i>OpCode</i> is set to a value other than <b>wlan_intf_opcode_autoconf_enabled</b>, <b>wlan_intf_opcode_background_scan_enabled</b>, <b>wlan_intf_opcode_media_streaming_mode</b>, <b>wlan_intf_opcode_bss_type</b>, or <b>wlan_intf_opcode_current_operation_mode</b>. The DACL is also not retrieved when <i>OpCode</i> is set to <b>wlan_intf_opcode_radio_state</b> and the caller is the console user.

For the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_ihv_control

The permissions for using the  <a href="https://msdn.microsoft.com/3fc32119-0f92-4939-8125-812f45584d45">WlanIhvControl</a> function for independent hardware vendor (IHV) control of WLAN drivers or services.

The DACL associated with this securable object is retrieved when <a href="https://msdn.microsoft.com/3fc32119-0f92-4939-8125-812f45584d45">WlanIhvControl</a>  is called. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_all_user_profiles_order

The permissions for modifying the order of all-user profiles.

The DACL associated with this securable object is retrieved before  <a href="https://msdn.microsoft.com/980c7920-a25e-4e05-a742-77178a7f000a">WlanSetProfileList</a> or <a href="https://msdn.microsoft.com/06ef9f55-b425-4f61-9b9e-3c27cc3796f6">WlanSetProfilePosition</a> performs an operation that changes the relative order of all-user profiles in the profile list  or moves an all-user profile to a lower position in the profile list. For either call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.  


### -field wlan_secure_add_new_all_user_profiles

The permissions for adding new all-user profiles.

<div class="alert"><b>Note</b>  The security descriptor associated with this object is applied to new all-user profiles created.</div>
<div> </div>
The DACL associated with this securable object is retrieved when <a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>  is called with <i>dwFlags</i> set to 0. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_add_new_per_user_profiles

The permissions for adding new per-user profiles.

The DACL associated with this securable object is retrieved when <a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>  is called with <i>dwFlags</i> set to WLAN_PROFILE_USER. For the call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_media_streaming_mode_enabled

The permissions for setting or querying the media streaming mode.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_media_streaming_mode</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_current_operation_mode

The permissions for setting or querying the operation mode of the wireless interface.

The DACL associated with this securable object is retrieved when either <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> or <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> is called with <i>OpCode</i> set to <b>wlan_intf_opcode_current_operation_mode</b>. For the <b>WlanQueryInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_READ_ACCESS permission to the access token of the calling thread. For the  <b>WlanSetInterface</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread.


### -field wlan_secure_get_plaintext_key

The permissions for retrieving the plain text key from a wireless profile.

 The DACL associated with this securable object is retrieved when the <a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a> function is called with the <b>WLAN_PROFILE_GET_PLAINTEXT_KEY</b>  flag set in the value pointed to by the <i>pdwFlags</i> parameter on input. For the <b>WlanGetProfile</b> call to succeed, the DACL must contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local computer.



<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.  




### -field wlan_secure_hosted_network_elevated_access

The permissions that have elevated access to call the privileged Hosted Network functions.  

The DACL associated with this securable object is retrieved when the  <a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a> function is called with the <i>OpCode</i> parameter set to <b>wlan_hosted_network_opcode_enable</b>. For the <b>WlanHostedNetworkSetProperty</b> call to succeed, the DACL must contain an ACE that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread. By default,  the permission to set the wireless Hosted Network property to <b>wlan_hosted_network_opcode_enable</b> is allowed only to the members of the Administrators group on a local computer.



 The DACL associated with this securable object is retrieved when the <a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a> function is called. For the <b>WlanHostedNetworkForceStart</b> call to succeed, the DACL must contain an ACE that grants <b>WLAN_WRITE_ACCESS</b> permission to the access token of the calling thread. By default,  the permission to force start the wireless Hosted Network is allowed only to the members of the Administrators group on a local computer.



<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.  


### -field wlan_secure_virtual_station_extensibility



<b>Windows 7:  </b>This value is an extension to native wireless APIs added on Windows 7 and  later.  


### -field wlan_secure_wfd_elevated_access

This value is reserved for internal use by the Wi-Fi Direct service.  

<b>Windows 8:  </b>This value is an extension to native wireless APIs added on Windows 8 and  later.  


### -field WLAN_SECURABLE_OBJECT_COUNT




## -remarks



These objects can be secured using <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a>. The current permissions associated with these objects can be retrieved using <a href="https://msdn.microsoft.com/5e14a70c-c049-4cd1-8675-2b01ed11463f">WlanGetSecuritySettings</a>. For more information about the use of securable objects, see <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How DACLs Control Access to an Object</a> and <a href="https://msdn.microsoft.com/cfea9f7d-a069-497b-8138-b3949002fa5d">Native Wifi API Permissions</a>.




## -see-also




<a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How DACLs Control Access to an Object</a>



<a href="https://msdn.microsoft.com/cfea9f7d-a069-497b-8138-b3949002fa5d">Native Wifi API Permissions</a>



<a href="https://msdn.microsoft.com/3ea88e52-34bb-47a6-b345-c789d1d8047d">WlanGetFilterList</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a>



<a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a>



<a href="https://msdn.microsoft.com/3fc32119-0f92-4939-8125-812f45584d45">WlanIhvControl</a>



<a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>



<a href="https://msdn.microsoft.com/4f2514be-f05e-4be6-8c74-ef7a9ffe1c53">WlanSetAutoConfigParameter</a>



<a href="https://msdn.microsoft.com/697682c9-cb26-42d6-86b5-d7adebcedc68">WlanSetFilterList</a>



<b>WlanSetInterface</b>



<a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>



<a href="https://msdn.microsoft.com/980c7920-a25e-4e05-a742-77178a7f000a">WlanSetProfileList</a>



<a href="https://msdn.microsoft.com/06ef9f55-b425-4f61-9b9e-3c27cc3796f6">WlanSetProfilePosition</a>
 

 

