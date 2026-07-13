---
UID: NF:wlanapi.WlanHostedNetworkForceStart
title: WlanHostedNetworkForceStart function (wlanapi.h)
description: Transitions the wireless Hosted Network to the wlan_hosted_network_active state without associating the request with the application's calling handle.
helpviewer_keywords: ["WlanHostedNetworkForceStart","WlanHostedNetworkForceStart function [NativeWIFI]","nwifi.wlanhostednetworkforcestart","wlanapi/WlanHostedNetworkForceStart"]
old-location: nwifi\wlanhostednetworkforcestart.htm
tech.root: nwifi
ms.assetid: d3e3b44f-ff52-4062-b54d-a0e3f2cf7785
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkForceStart, WlanHostedNetworkForceStart function [NativeWIFI], nwifi.wlanhostednetworkforcestart, wlanapi/WlanHostedNetworkForceStart
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
 - WlanHostedNetworkForceStart
 - wlanapi/WlanHostedNetworkForceStart
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
 - WlanHostedNetworkForceStart
---

# WlanHostedNetworkForceStart function


## -description

The <b>WlanHostedNetworkForceStart</b> function transitions the wireless Hosted Network to the <b>wlan_hosted_network_active state</b> without associating the request with the application's calling handle.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason  if the call to the <b>WlanHostedNetworkForceStart</b> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
The caller does not have sufficient permissions. 

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
The resource is not in the correct state to perform the requested operation.

This error is returned if the wireless Hosted Network is disabled by group policy on a domain.

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

The <b>WlanHostedNetworkForceStart</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkForceStart</b> function to force the start of the wireless Hosted Network by transitioning the wireless Hosted Network to the <b>wlan_hosted_network_active state</b> without associating the request with the application's calling handle. A successful call to the <b>WlanHostedNetworkForceStart</b> function should eventually be matched by a call to <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestop">WlanHostedNetworkForceStop</a> function.
Any Hosted Network state change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


The cost of calling the <b>WlanHostedNetworkForceStart</b> function over calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkstartusing">WlanHostedNetworkStartUsing</a> is the associated privilege required. An application might call the <b>WlanHostedNetworkForceStart</b> function after ensuring that an elevated system user accepts the increased power requirements involved in running the wireless Hosted Network for extended durations.

The <b>WlanHostedNetworkForceStart</b> function could fail if Hosted Network state is <b>wlan_hosted_network_unavailable</b> or the caller does not have sufficient privileges.

This function to force the start of the Hosted Network can only be called if the user has the appropriate associated privilege. Permissions are stored in a discretionary access control list (DACL) associated with a <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a>.  To call the <b>WlanHostedNetworkForceStart</b>, the client access token of the caller must have elevated privileges exposed by the following enumeration in <b>WLAN_SECURABLE_OBJECT</b>: <ul>
<li><b>wlan_secure_hosted_network_elevated_access</b></li>
</ul>


The ability to enable the wireless Hosted Network may also be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestop">WlanHostedNetworkForceStop</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkstartusing">WlanHostedNetworkStartUsing</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkstopusing">WlanHostedNetworkStopUsing</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>