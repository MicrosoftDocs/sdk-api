---
UID: NF:wlanapi.WlanHostedNetworkRefreshSecuritySettings
title: WlanHostedNetworkRefreshSecuritySettings function (wlanapi.h)
description: Refreshes the configurable and auto-generated parts of the wireless Hosted Network security settings.
helpviewer_keywords: ["WlanHostedNetworkRefreshSecuritySettings","WlanHostedNetworkRefreshSecuritySettings function [NativeWIFI]","nwifi.wlanhostednetworkrefreshsecuritysettings","wlanapi/WlanHostedNetworkRefreshSecuritySettings"]
old-location: nwifi\wlanhostednetworkrefreshsecuritysettings.htm
tech.root: nwifi
ms.assetid: 9589e3a6-6e7a-4186-bfd0-a942a39ecafb
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkRefreshSecuritySettings, WlanHostedNetworkRefreshSecuritySettings function [NativeWIFI], nwifi.wlanhostednetworkrefreshsecuritysettings, wlanapi/WlanHostedNetworkRefreshSecuritySettings
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
 - WlanHostedNetworkRefreshSecuritySettings
 - wlanapi/WlanHostedNetworkRefreshSecuritySettings
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
 - WlanHostedNetworkRefreshSecuritySettings
---

# WlanHostedNetworkRefreshSecuritySettings function


## -description

The <b>WlanHostedNetworkRefreshSecuritySettings</b> function refreshes the configurable and auto-generated parts of the wireless Hosted Network security settings.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <b>WlanHostedNetworkRefreshSecuritySettings</b> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
The resource is not in the correct state to perform the requested operation.

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

The <b>WlanHostedNetworkRefreshSecuritySettings</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkRefreshSecuritySettings</b> function to force a refresh of the configurable and auto-generated parts of the security settings (the primary key) on the wireless Hosted Network. 

An application might call the <b>WlanHostedNetworkRefreshSecuritySettings</b> function after ensuring that the user accepts the impact of updating the security settings. In order to succeed,  this function must persist the new settings which would require that Hosted Network state be transitioned to wlan_hosted_network_idle if it was currently running (wlan_hosted_network_active). 

<div class="alert"><b>Note</b>  Any network clients (PCs or devices) on the wireless Hosted Network would have to be re-configured after calling the <b>WlanHostedNetworkRefreshSecuritySettings</b> function if their continued usage is a goal. An application would typically call this function in situations where the user feels that the security of the previous primary key used for security by the wireless Hosted Network has been violated. Note that the <b>WlanHostedNetworkRefreshSecuritySettings</b> function does not change or reset the secondary key.</div>
<div> </div>
Any Hosted Network state change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


Any user can call the <b>WlanHostedNetworkRefreshSecuritySettings</b> function to refresh the security settings on the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkinitsettings">WlanHostedNetworkInitSettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey">WlanHostedNetworkSetSecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>