---
UID: NF:wlanapi.WlanSetSecuritySettings
title: WlanSetSecuritySettings function (wlanapi.h)
description: Sets the security settings for a configurable object.
helpviewer_keywords: ["WlanSetSecuritySettings","WlanSetSecuritySettings function [NativeWIFI]","nwifi.wlansetsecuritysettings","wlanapi/WlanSetSecuritySettings"]
old-location: nwifi\wlansetsecuritysettings.htm
tech.root: nwifi
ms.assetid: 6038e4bc-7f07-4148-ac34-e290c8c40e99
ms.date: 12/05/2018
ms.keywords: WlanSetSecuritySettings, WlanSetSecuritySettings function [NativeWIFI], nwifi.wlansetsecuritysettings, wlanapi/WlanSetSecuritySettings
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
 - WlanSetSecuritySettings
 - wlanapi/WlanSetSecuritySettings
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
 - WlanSetSecuritySettings
---

# WlanSetSecuritySettings function


## -description

The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a> function sets the security settings for a configurable object.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param SecurableObject [in]

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a> value that specifies the object to which the security settings will be applied.

### -param strModifiedSDDL [in]

A security descriptor string that specifies the new security settings for the object. This string must be NULL-terminated. For more information, see the Remarks section.

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
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>strModifiedSDDL</i> is <b>NULL</b>.</li>
<li><i>SecurableObject</i> is set to a value greater than or equal to <b>WLAN_SECURABLE_OBJECT_COUNT</b> (12).</li>
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
A handle is invalid. This error is returned if the handle specified in the <i>hClientHandle</i>  parameter was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions. 

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
</table>

## -remarks

A successful call to the <b>WlanSetSecuritySettings</b> function overrides the default permissions associated with an object. For more information about default permissions, see <a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>.

The following describes the procedure for creating a security descriptor object and parsing it as a string.

<ol>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a> to create a security descriptor in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a> to set the owner information for the security descriptor.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a> to create a discretionary access control list (DACL) in memory.</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a> or <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a> to add access control entries (ACEs) to the DACL. Set the <i>AccessMask</i> parameter to one of the following bitwise OR combinations as appropriate:<ul>
<li>WLAN_READ_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS | WLAN_WRITE_ACCESS</li>
</ul>
</li>
<li>Call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a> to add the DACL to the security descriptor.</li>
<li>Call <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> to convert the descriptor to string.</li>
</ol>
The string returned by <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> can then be used as the <i>strModifiedSDDL</i> parameter value when calling <b>WlanSetSecuritySettings</b>.

## -see-also

<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings">WlanGetSecuritySettings</a>