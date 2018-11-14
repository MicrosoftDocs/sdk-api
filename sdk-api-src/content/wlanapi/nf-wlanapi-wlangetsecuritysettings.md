---
UID: NF:wlanapi.WlanGetSecuritySettings
title: WlanGetSecuritySettings function
author: windows-sdk-content
description: Gets the security settings associated with a configurable object.
old-location: nwifi\wlangetsecuritysettings.htm
tech.root: NativeWiFi
ms.assetid: 5e14a70c-c049-4cd1-8675-2b01ed11463f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WlanGetSecuritySettings, WlanGetSecuritySettings function [NativeWIFI], nwifi.wlangetsecuritysettings, wlan_opcode_value_type_set_by_group_policy, wlan_opcode_value_type_set_by_user, wlanapi/WlanGetSecuritySettings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanGetSecuritySettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WlanGetSecuritySettings
: 
---

# WlanGetSecuritySettings function


## -description


The <b>WlanGetSecuritySettings</b> function gets the security settings associated with a configurable object.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param SecurableObject [in]

A <a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a> value that specifies the object to which the security settings apply.


### -param pValueType [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/36f74ee5-499e-4d3d-ae32-a57c5e3b2eac">WLAN_OPCODE_VALUE_TYPE</a> value that specifies the source of the security settings.

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
The security settings were set by the user. A user can set security settings by calling <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a>.

</td>
</tr>
</table>
 


### -param pstrCurrentSDDL [out]

On input, this parameter must be <b>NULL</b>. 

On output, this parameter receives a pointer to the security descriptor string that specifies the security settings for the object if the function call succeeds. For more information about this string, see <a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a> function.


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



The caller is responsible for freeing the memory allocated to the security descriptor string pointed to by the <i>pstrCurrentSDDL</i> parameter if the function succeeds. When no longer needed, the memory for the security descriptor string should be freed by calling <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function and passing in the <i>pstrCurrentSDDL</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/cfea9f7d-a069-497b-8138-b3949002fa5d">Native Wifi API Permissions</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>



<a href="https://msdn.microsoft.com/6038e4bc-7f07-4148-ac34-e290c8c40e99">WlanSetSecuritySettings</a>
 

 

