---
UID: NF:wlanapi.WlanHostedNetworkSetProperty
title: WlanHostedNetworkSetProperty function
author: windows-sdk-content
description: Sets static properties of the wireless Hosted Network.
old-location: nwifi\wlanhostednetworksetproperty.htm
old-project: nativewifi
ms.assetid: 88139383-f5d5-4e42-b41e-ea754a89356d
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WlanHostedNetworkSetProperty, WlanHostedNetworkSetProperty function [NativeWIFI], nwifi.wlanhostednetworksetproperty, wlan_hosted_network_opcode_connection_settings, wlan_hosted_network_opcode_enable, wlanapi/WlanHostedNetworkSetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanHostedNetworkSetProperty
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanHostedNetworkSetProperty function


## -description


The <b>WlanHostedNetworkSetProperty</b> function sets static properties of the wireless Hosted Network. 


## -parameters




### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param OpCode [in]

The identifier for the property to be set. This identifier can only be the following values in the <a href="https://msdn.microsoft.com/e4acd7ad-c8f2-4ece-8d27-ced879baa9e7">WLAN_HOSTED_NETWORK_OPCODE</a> enumeration defined in the <i>Wlanapi.h </i>header file:



##### )



##### )


### -param dwDataSize [in]

A value that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. 


### -param pvData [in]

A pointer to a buffer with the static property to set.  The data type associated with this buffer depends upon the value of <i>OpCode</i> parameter. 


### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <b>WlanHostedNetworkSetProperty</b> function fails. Possible values for the failure reason are from the <a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i>header file.


### -param pvReserved

Reserved for future use. This parameter must be <b>NULL</b>.


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
The caller does not have sufficient permissions. This error is also returned if the <i>OpCode</i> parameter  was <b>wlan_hosted_network_opcode_enable</b> and the wireless Hosted Network is disabled by group policy on a domain. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The network connection profile used by the wireless Hosted Network is corrupted.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>OpCode</i> is not one of the enumerated values defined in the <a href="https://msdn.microsoft.com/e4acd7ad-c8f2-4ece-8d27-ced879baa9e7">WLAN_HOSTED_NETWORK_OPCODE</a>.</li>
<li><i>dwDataSize</i> is zero.</li>
<li><i>pvData</i> is <b>NULL</b>.</li>
<li><i>pvData</i> does not point to a well- formed static property.</li>
<li><i>pvReserved</i> is not <b>NULL</b>.</li>
</ul>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The resource is not in the correct state to perform the requested operation. This can occur if the wireless Hosted Network was in the process of shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the application calls the <a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a> function with the <i>OpCode</i> parameter set to  <b>wlan_hosted_network_opcode_station_profile</b> or <b>wlan_hosted_network_opcode_security_settings</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service has not been started. This error is returned if the WLAN AutoConfig Service is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Various RPC and other error codes. Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -remarks



The <b>WlanHostedNetworkSetProperty</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkSetProperty</b> function to set the current static properties of the wireless Hosted Network. 
Any Hosted Network property change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


The data type associated with the buffer pointed to by the <i>pvData</i> parameter depends upon the value of <i>OpCode</i> parameter as follows: 



<table>
<tr>
<th>OpCode</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_opcode_connection_settings"></a><a id="WLAN_HOSTED_NETWORK_OPCODE_CONNECTION_SETTINGS"></a>wlan_hosted_network_opcode_connection_settings

</td>
<td width="60%">
A pointer to a <a href="https://msdn.microsoft.com/845eaef2-7ce0-4d7a-8273-8b843b5c95fd">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a> structure is passed in the <i>pvData</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_opcode_enable"></a><a id="WLAN_HOSTED_NETWORK_OPCODE_ENABLE"></a>wlan_hosted_network_opcode_enable

</td>
<td width="60%">
A pointer to <b>BOOL</b> is passed in the <i>pvData</i> parameter.

</td>
</tr>
</table>
 

If the <b>WlanHostedNetworkSetProperty</b> function is called with the <i>OpCode</i> parameter set to <b>wlan_hosted_network_opcode_enable</b>, the user must have the appropriate associated privilege. Permissions are stored in a discretionary access control list (DACL) associated with a <a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a>.  To call the  <b>WlanHostedNetworkSetProperty</b> function with the <i>OpCode</i> parameter of <b>wlan_hosted_network_opcode_enable</b>, the client access token of the caller must have elevated privileges exposed by the following enumeration in <b>WLAN_SECURABLE_OBJECT</b>: <ul>
<li><b>wlan_secure_hosted_network_elevated_access</b></li>
</ul>


If the <b>WlanHostedNetworkSetProperty</b> function is passed any of the following values in the <i>OpCode</i> parameter, the function will fail with <b>ERROR_NOT_SUPPORTED</b>: <ul>
<li>wlan_hosted_network_opcode_station_profile</li>
<li>wlan_hosted_network_opcode_connection_settings</li>
</ul>


In order to succeed,  the <b>WlanHostedNetworkSetProperty</b> function must persist the new settings which requires that the Hosted Network state be transitioned to <b>wlan_hosted_network_idle</b> if it was currently running (wlan_hosted_network_active). 

Any user can call this function to set the Hosted Network properties. However, to set the <b>wlan_hosted_network_opcode_enable</b> flag requires elevated privileges. The ability to enable the wireless Hosted Network may also be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/56e86ef8-f759-4e56-a591-74e03430125a">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="https://msdn.microsoft.com/845eaef2-7ce0-4d7a-8273-8b843b5c95fd">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a>



<a href="https://msdn.microsoft.com/e4acd7ad-c8f2-4ece-8d27-ced879baa9e7">WLAN_HOSTED_NETWORK_OPCODE</a>



<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/aed4db5d-9740-43ee-bf09-7a4a5abae953">WlanHostedNetworkInitSettings</a>



<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/5989977a-7a2f-43b8-a958-058db01fd24f">WlanHostedNetworkQuerySecondaryKey</a>



<a href="https://msdn.microsoft.com/9589e3a6-6e7a-4186-bfd0-a942a39ecafb">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="https://msdn.microsoft.com/385148fd-b5cd-4221-be25-077f484e93e9">WlanHostedNetworkSetSecondaryKey</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>
 

 

