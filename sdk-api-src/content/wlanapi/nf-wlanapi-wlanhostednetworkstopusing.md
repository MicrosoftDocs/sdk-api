---
UID: NF:wlanapi.WlanHostedNetworkStopUsing
title: WlanHostedNetworkStopUsing function (wlanapi.h)
description: Stops the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkStopUsing","WlanHostedNetworkStopUsing function [NativeWIFI]","nwifi.wlanhostednetworkstopusing","wlanapi/WlanHostedNetworkStopUsing"]
old-location: nwifi\wlanhostednetworkstopusing.htm
tech.root: nwifi
ms.assetid: 36b5ed93-33c4-4ade-a6d9-0d240854a5ef
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkStopUsing, WlanHostedNetworkStopUsing function [NativeWIFI], nwifi.wlanhostednetworkstopusing, wlanapi/WlanHostedNetworkStopUsing
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
 - WlanHostedNetworkStopUsing
 - wlanapi/WlanHostedNetworkStopUsing
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
 - WlanHostedNetworkStopUsing
---

# WlanHostedNetworkStopUsing function


## -description

The <b>WlanHostedNetworkStopUsing</b> function stops the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason  if the call to the <b>WlanHostedNetworkStopUsing</b> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
The resource is not in the correct state to perform the requested operation. This can occur if the wireless Hosted Network was in the process of shutting down.

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

The <b>WlanHostedNetworkStopUsing</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

An application calls the <b>WlanHostedNetworkStopUsing</b> function to stop the Hosted Network. A application calls the <b>WlanHostedNetworkStopUsing</b> function to match earlier successful calls to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkstartusing">WlanHostedNetworkStartUsing</a> function. The wireless Hosted Network will remain active until all applications have called the <b>WlanHostedNetworkStopUsing</b> function or the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestop">WlanHostedNetworkForceStop</a> function is called to force a stop. When the wireless Hosted Network has stopped, the state switches to <b>wlan_hosted_network_idle</b>. This call could also fail if the Hosted Network state changed because of external events (for example, if the miniport driver for the wireless interface card becomes unavailable). 

Any user can call this function to stop the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestart">WlanHostedNetworkForceStart</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkforcestop">WlanHostedNetworkForceStop</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkstartusing">WlanHostedNetworkStartUsing</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>