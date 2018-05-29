---
UID: NF:wlanapi.WlanSetSecuritySettings
title: WlanSetSecuritySettings function
author: windows-sdk-content
description: Sets the security settings for a configurable object.
old-location: nwifi\wlansetsecuritysettings.htm
old-project: NativeWiFi
ms.assetid: 6038e4bc-7f07-4148-ac34-e290c8c40e99
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: WlanSetSecuritySettings, WlanSetSecuritySettings function [NativeWIFI], nwifi.wlansetsecuritysettings, wlanapi/WlanSetSecuritySettings
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wlanapi.dll
api_name:
-	WlanSetSecuritySettings
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanSetSecuritySettings function


## -description


The <a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a> function sets the security settings for a configurable object.   


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param SecurableObject [in]

A <a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a> value that specifies the object to which the security settings will be applied.


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



A successful call to the <b>WlanSetSecuritySettings</b> function overrides the default permissions associated with an object. For more information about default permissions, see <a href="https://msdn.microsoft.com/cfea9f7d-a069-497b-8138-b3949002fa5d">Native Wifi API Permissions</a>.

The following describes the procedure for creating a security descriptor object and parsing it as a string.

<ol>
<li>Call <a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a> to create a security descriptor in memory.</li>
<li>Call <a href="https://msdn.microsoft.com/cb3ba617-322a-4b8c-a9d5-32910315fb56">SetSecurityDescriptorOwner</a> to set the owner information for the security descriptor.</li>
<li>Call <a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a> to create a discretionary access control list (DACL) in memory.</li>
<li>Call <a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a> or <a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a> to add access control entries (ACEs) to the DACL. Set the <i>AccessMask</i> parameter to one of the following bitwise OR combinations as appropriate:<ul>
<li>WLAN_READ_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS</li>
<li>WLAN_READ_ACCESS | WLAN_EXECUTE_ACCESS | WLAN_WRITE_ACCESS</li>
</ul>
</li>
<li>Call <a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a> to add the DACL to the security descriptor.</li>
<li>Call <a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a> to convert the descriptor to string.</li>
</ol>
The string returned by <a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a> can then be used as the <i>strModifiedSDDL</i> parameter value when calling <b>WlanSetSecuritySettings</b>.




## -see-also




<a href="https://msdn.microsoft.com/cfea9f7d-a069-497b-8138-b3949002fa5d">Native Wifi API Permissions</a>



<a href="https://msdn.microsoft.com/5e14a70c-c049-4cd1-8675-2b01ed11463f">WlanGetSecuritySettings</a>
 

 

