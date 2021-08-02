---
UID: NF:wlanapi.WlanHostedNetworkSetProperty
title: WlanHostedNetworkSetProperty function (wlanapi.h)
description: Sets static properties of the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkSetProperty","WlanHostedNetworkSetProperty function [NativeWIFI]","nwifi.wlanhostednetworksetproperty","wlan_hosted_network_opcode_connection_settings","wlan_hosted_network_opcode_enable","wlanapi/WlanHostedNetworkSetProperty"]
old-location: nwifi\wlanhostednetworksetproperty.htm
tech.root: nwifi
ms.assetid: 88139383-f5d5-4e42-b41e-ea754a89356d
ms.date: 11/19/2020
ms.keywords: WlanHostedNetworkSetProperty, WlanHostedNetworkSetProperty function [NativeWIFI], nwifi.wlanhostednetworksetproperty, wlan_hosted_network_opcode_connection_settings, wlan_hosted_network_opcode_enable, wlanapi/WlanHostedNetworkSetProperty
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlanHostedNetworkSetProperty
 - wlanapi/WlanHostedNetworkSetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanHostedNetworkSetProperty
---

# WlanHostedNetworkSetProperty function


## -description

The <b>WlanHostedNetworkSetProperty</b> function sets static properties of the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param OpCode [in]

The identifier for the property to be set. This identifier can only be the following values in the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_opcode">WLAN_HOSTED_NETWORK_OPCODE</a> enumeration defined in the <i>Wlanapi.h </i> header file:

* **wlan_hosted_network_opcode_connection_settings**

The Hosted Network connection settings.

* **wlan_hosted_network_opcode_enable**

The Hosted Network enabled flag.



### -param dwDataSize [in]

A value that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter.

### -param pvData [in]

A pointer to a buffer with the static property to set.  The data type associated with this buffer depends upon the value of <i>OpCode</i> parameter.

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <b>WlanHostedNetworkSetProperty</b> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
<li><i>OpCode</i> is not one of the enumerated values defined in the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_opcode">WLAN_HOSTED_NETWORK_OPCODE</a>.</li>
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
The request is not supported. This error is returned if the application calls the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a> function with the <i>OpCode</i> parameter set to  <b>wlan_hosted_network_opcode_station_profile</b> or <b>wlan_hosted_network_opcode_security_settings</b>. 

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>

## -remarks

The <b>WlanHostedNetworkSetProperty</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkSetProperty</b> function to set the current static properties of the wireless Hosted Network. 
Any Hosted Network property change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


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
A pointer to a <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a> structure is passed in the <i>pvData</i> parameter.

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
 

If the <b>WlanHostedNetworkSetProperty</b> function is called with the <i>OpCode</i> parameter set to <b>wlan_hosted_network_opcode_enable</b>, the user must have the appropriate associated privilege. Permissions are stored in a discretionary access control list (DACL) associated with a <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a>.  To call the  <b>WlanHostedNetworkSetProperty</b> function with the <i>OpCode</i> parameter of <b>wlan_hosted_network_opcode_enable</b>, the client access token of the caller must have elevated privileges exposed by the following enumeration in <b>WLAN_SECURABLE_OBJECT</b>: <ul>
<li><b>wlan_secure_hosted_network_elevated_access</b></li>
</ul>


If the <b>WlanHostedNetworkSetProperty</b> function is passed any of the following values in the <i>OpCode</i> parameter, the function will fail with <b>ERROR_NOT_SUPPORTED</b>: <ul>
<li>wlan_hosted_network_opcode_station_profile</li>
<li>wlan_hosted_network_opcode_connection_settings</li>
</ul>


In order to succeed,  the <b>WlanHostedNetworkSetProperty</b> function must persist the new settings which requires that the Hosted Network state be transitioned to <b>wlan_hosted_network_idle</b> if it was currently running (wlan_hosted_network_active). 

Any user can call this function to set the Hosted Network properties. However, to set the <b>wlan_hosted_network_opcode_enable</b> flag requires elevated privileges. The ability to enable the wireless Hosted Network may also be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_opcode">WLAN_HOSTED_NETWORK_OPCODE</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkinitsettings">WlanHostedNetworkInitSettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey">WlanHostedNetworkQuerySecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey">WlanHostedNetworkSetSecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>