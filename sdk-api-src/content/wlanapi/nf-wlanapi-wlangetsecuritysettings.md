---
UID: NF:wlanapi.WlanGetSecuritySettings
title: WlanGetSecuritySettings function (wlanapi.h)
description: Gets the security settings associated with a configurable object.
helpviewer_keywords: ["WlanGetSecuritySettings","WlanGetSecuritySettings function [NativeWIFI]","nwifi.wlangetsecuritysettings","wlan_opcode_value_type_set_by_group_policy","wlan_opcode_value_type_set_by_user","wlanapi/WlanGetSecuritySettings"]
old-location: nwifi\wlangetsecuritysettings.htm
tech.root: nwifi
ms.assetid: 5e14a70c-c049-4cd1-8675-2b01ed11463f
ms.date: 12/05/2018
ms.keywords: WlanGetSecuritySettings, WlanGetSecuritySettings function [NativeWIFI], nwifi.wlangetsecuritysettings, wlan_opcode_value_type_set_by_group_policy, wlan_opcode_value_type_set_by_user, wlanapi/WlanGetSecuritySettings
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
 - WlanGetSecuritySettings
 - wlanapi/WlanGetSecuritySettings
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
 - WlanGetSecuritySettings
---

# WlanGetSecuritySettings function


## -description

The <b>WlanGetSecuritySettings</b> function gets the security settings associated with a configurable object.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param SecurableObject [in]

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a> value that specifies the object to which the security settings apply.

### -param pValueType [out, optional]

A pointer to a <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a> value that specifies the source of the security settings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="wlan_opcode_value_type_set_by_group_policy"></a><a id="WLAN_OPCODE_VALUE_TYPE_SET_BY_GROUP_POLICY"></a><dl>
<dt><b>wlan_opcode_value_type_set_by_group_policy</b></dt>
</dl>
</td>
<td width="60%">
The security settings were set by group policy.

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_opcode_value_type_set_by_user"></a><a id="WLAN_OPCODE_VALUE_TYPE_SET_BY_USER"></a><dl>
<dt><b>wlan_opcode_value_type_set_by_user</b></dt>
</dl>
</td>
<td width="60%">
The security settings were set by the user. A user can set security settings by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a>.

</td>
</tr>
</table>

### -param pstrCurrentSDDL [out]

On input, this parameter must be <b>NULL</b>. 

On output, this parameter receives a pointer to the security descriptor string that specifies the security settings for the object if the function call succeeds. For more information about this string, see <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a> function.

### -param pdwGrantedAccess [out]

The access mask of the object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_READ_ACCESS</dt>
</dl>
</td>
<td width="60%">
The caller can view the object's permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_EXECUTE_ACCESS</dt>
</dl>
</td>
<td width="60%">
The caller can read from and execute the object. WLAN_EXECUTE_ACCESS has the same value as the bitwise OR combination WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_WRITE_ACCESS</dt>
</dl>
</td>
<td width="60%">
The caller can read from, execute, and write to the object. WLAN_WRITE_ACCESS has the same value as the bitwise OR combination WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS | WLAN_WRITE_ACCESS.

</td>
</tr>
</table>

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
<li><i>pstrCurrentSDDL</i> is <b>NULL</b>.</li>
<li><i>pdwGrantedAccess</i> is <b>NULL</b>.</li>
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

The caller is responsible for freeing the memory allocated to the security descriptor string pointed to by the <i>pstrCurrentSDDL</i> parameter if the function succeeds. When no longer needed, the memory for the security descriptor string should be freed by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function and passing in the <i>pstrCurrentSDDL</i> parameter.

## -see-also

<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings">WlanSetSecuritySettings</a>