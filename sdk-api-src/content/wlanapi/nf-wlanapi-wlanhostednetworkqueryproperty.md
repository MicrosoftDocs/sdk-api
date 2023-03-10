---
UID: NF:wlanapi.WlanHostedNetworkQueryProperty
title: WlanHostedNetworkQueryProperty function (wlanapi.h)
description: Queries the current static properties of the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkQueryProperty","WlanHostedNetworkQueryProperty function [NativeWIFI]","nwifi.wlanhostednetworkqueryproperty","wlanapi/WlanHostedNetworkQueryProperty"]
old-location: nwifi\wlanhostednetworkqueryproperty.htm
tech.root: nwifi
ms.assetid: bab05629-c921-4639-94db-25f77742dbd3
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkQueryProperty, WlanHostedNetworkQueryProperty function [NativeWIFI], nwifi.wlanhostednetworkqueryproperty, wlanapi/WlanHostedNetworkQueryProperty
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
 - WlanHostedNetworkQueryProperty
 - wlanapi/WlanHostedNetworkQueryProperty
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
 - WlanHostedNetworkQueryProperty
---

# WlanHostedNetworkQueryProperty function


## -description

The <b>WlanHostedNetworkQueryProperty</b> function queries the current static properties of the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param OpCode [in]

The identifier for property to be queried. This identifier can be any of the values in the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_opcode">WLAN_HOSTED_NETWORK_OPCODE</a> enumeration defined in the <i>Wlanapi.h </i> header file.

### -param pdwDataSize [out]

A pointer to a value that specifies the size, in bytes, of the buffer returned in the <i>ppvData</i> parameter, if the call to the <b>WlanHostedNetworkQueryProperty</b> function succeeds.

### -param ppvData [out]

On input, this parameter must be <b>NULL</b>. 

On output, this parameter receives a pointer to a buffer returned with the static property requested,  if the call to the <b>WlanHostedNetworkQueryProperty</b> function succeeds.  The data type associated with this buffer depends upon the value of <i>OpCode</i> parameter.

### -param pWlanOpcodeValueType [out]

A pointer to a value that receives the value type of the wireless Hosted Network property,  if the call to the <b>WlanHostedNetworkQueryProperty</b> function succeeds. The returned value is an enumerated type in the <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a> enumeration defined in the <i>Wlanapi.h </i> header file.

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
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data for the wireless Hosted Network is unconfigured.  This error is returned if the application calls the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a> function with the <i>OpCode</i> parameter set to  <b>wlan_hosted_network_opcode_station_profile</b> or <b>wlan_hosted_network_opcode_connection_settings</b> before a SSID is configured in the wireless Hosted Network.

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
<li><i>pdwDataSize</i> is <b>NULL</b>.</li>
<li><i>ppvData</i> is <b>NULL</b>.</li>
<li><i>pWlanOpcodeValueType</i> is <b>NULL</b>.</li>
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
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to complete this operation. 

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

The <b>WlanHostedNetworkQueryProperty</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkQueryProperty</b> function to query the current static properties of the wireless Hosted Network. This function does not change the state or properties of the wireless Hosted Network.

If the function succeeds, the <i>ppvData</i> parameter points to a buffer that contains the requested property. The size of this buffer is returned in a pointer returned in the <i>pwdDataSize</i> parameter. The <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a> is returned in a pointer returned in the <i>pWlanOpcodeValueType</i> parameter. The memory used for the buffer in the <i>ppvData</i> parameter that is returned should be released by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function after the buffer is no longer needed.

The data type associated with the buffer pointed to by the <i>ppvData</i> parameter depends upon the value of <i>OpCode</i> parameter as follows: 



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
A pointer to a <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a> structure is returned.

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_opcode_security_settings"></a><a id="WLAN_HOSTED_NETWORK_OPCODE_SECURITY_SETTINGS"></a>wlan_hosted_network_opcode_security_settings

</td>
<td width="60%">
A pointer to a <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_security_settings">WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</a> structure is returned.

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_opcode_station_profile"></a><a id="WLAN_HOSTED_NETWORK_OPCODE_STATION_PROFILE"></a>wlan_hosted_network_opcode_station_profile

</td>
<td width="60%">
A <b>PWSTR</b> to contains an XML WLAN profile for connecting to the wireless Hosted Network is returned.

</td>
</tr>
<tr>
<td width="40%">
<a id="wlan_hosted_network_opcode_enable"></a><a id="WLAN_HOSTED_NETWORK_OPCODE_ENABLE"></a>wlan_hosted_network_opcode_enable

</td>
<td width="60%">
A <b>PBOOL</b> that indicates if wireless Hosted Network is enabled is returned.

</td>
</tr>
</table>
 

If the <b>WlanHostedNetworkQueryProperty</b> function is passed any of the following values in the <i>OpCode</i> parameter before a SSID is configured in the wireless Hosted Network, the function will fail with <b>ERROR_BAD_CONFIGURATION</b>: <ul>
<li>wlan_hosted_network_opcode_station_profile</li>
<li>wlan_hosted_network_opcode_connection_settings</li>
</ul>


Any user can call the <b>WlanHostedNetworkQueryProperty</b> function to query the Hosted Network properties. 

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings">WLAN_HOSTED_NETWORK_CONNECTION_SETTINGS</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_opcode">WLAN_HOSTED_NETWORK_OPCODE</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_hosted_network_security_settings">WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkinitsettings">WlanHostedNetworkInitSettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey">WlanHostedNetworkQuerySecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey">WlanHostedNetworkSetSecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>