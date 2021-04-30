---
UID: NF:wlanapi.WlanHostedNetworkQueryStatus
title: WlanHostedNetworkQueryStatus function (wlanapi.h)
description: Queries the current status of the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkQueryStatus","WlanHostedNetworkQueryStatus function [NativeWIFI]","nwifi.wlanhostednetworkquerystatus","wlanapi/WlanHostedNetworkQueryStatus"]
old-location: nwifi\wlanhostednetworkquerystatus.htm
tech.root: nwifi
ms.assetid: 896cff65-74ec-41d5-89e3-95fa85fd54cd
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkQueryStatus, WlanHostedNetworkQueryStatus function [NativeWIFI], nwifi.wlanhostednetworkquerystatus, wlanapi/WlanHostedNetworkQueryStatus
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
 - WlanHostedNetworkQueryStatus
 - wlanapi/WlanHostedNetworkQueryStatus
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
 - WlanHostedNetworkQueryStatus
---

# WlanHostedNetworkQueryStatus function


## -description

The <b>WlanHostedNetworkQueryStatus</b> function queries the current status of the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param ppWlanHostedNetworkStatus [out]

On input, this parameter must be <b>NULL</b>. 

On output, this parameter receives a pointer to the current status of the wireless Hosted Network,  if the call to the <b>WlanHostedNetworkQueryStatus</b> function succeeds. The current status is returned in a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a> structure.

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
<li>ppWlanHostedNetworkStatus is <b>NULL</b>.</li>
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

The <b>WlanHostedNetworkQueryStatus</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkQueryStatus</b> function to query the current status of the wireless Hosted Network. This function does not change the state of the wireless Hosted Network. 

If the function succeeds, the <i>ppWlanHostedNetworkStatus</i> parameter points to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a> structure with the current status. The memory used for the <b>WLAN_HOSTED_NETWORK_STATUS</b> structure that is returned should be freed after use by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function.

Any user can call the <b>WlanHostedNetworkQueryStatus</b> function to query the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_hosted_network_status">WLAN_HOSTED_NETWORK_STATUS</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey">WlanHostedNetworkQuerySecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>