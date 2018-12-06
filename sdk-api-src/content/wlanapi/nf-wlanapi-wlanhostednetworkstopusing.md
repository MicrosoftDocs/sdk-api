---
UID: NF:wlanapi.WlanHostedNetworkStopUsing
title: WlanHostedNetworkStopUsing function
author: windows-sdk-content
description: Stops the wireless Hosted Network.
old-location: nwifi\wlanhostednetworkstopusing.htm
tech.root: NativeWiFi
ms.assetid: 36b5ed93-33c4-4ade-a6d9-0d240854a5ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WlanHostedNetworkStopUsing, WlanHostedNetworkStopUsing function [NativeWIFI], nwifi.wlanhostednetworkstopusing, wlanapi/WlanHostedNetworkStopUsing
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanHostedNetworkStopUsing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlanHostedNetworkStopUsing function


## -description


The <b>WlanHostedNetworkStopUsing</b> function stops the wireless Hosted Network.


## -parameters




### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason  if the call to the <b>WlanHostedNetworkStopUsing</b> function fails. Possible values for the failure reason are from the <a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i>header file.


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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -remarks



The <b>WlanHostedNetworkStopUsing</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

An application calls the <b>WlanHostedNetworkStopUsing</b> function to stop the Hosted Network. A application calls the <b>WlanHostedNetworkStopUsing</b> function to match earlier successful calls to the <a href="https://msdn.microsoft.com/923ffc09-f378-442c-a891-34b0c0d04c41">WlanHostedNetworkStartUsing</a> function. The wireless Hosted Network will remain active until all applications have called the <b>WlanHostedNetworkStopUsing</b> function or the <a href="https://msdn.microsoft.com/abcfc33d-0310-46d2-a543-5c9529c2b851">WlanHostedNetworkForceStop</a> function is called to force a stop. When the wireless Hosted Network has stopped, the state switches to <b>wlan_hosted_network_idle</b>. This call could also fail if the Hosted Network state changed because of external events (for example, if the miniport driver for the wireless interface card becomes unavailable). 

Any user can call this function to stop the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/56e86ef8-f759-4e56-a591-74e03430125a">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a>



<a href="https://msdn.microsoft.com/abcfc33d-0310-46d2-a543-5c9529c2b851">WlanHostedNetworkForceStop</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>



<a href="https://msdn.microsoft.com/923ffc09-f378-442c-a891-34b0c0d04c41">WlanHostedNetworkStartUsing</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>
 

 

