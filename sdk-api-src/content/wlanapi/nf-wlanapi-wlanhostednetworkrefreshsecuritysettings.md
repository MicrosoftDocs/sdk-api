---
UID: NF:wlanapi.WlanHostedNetworkRefreshSecuritySettings
title: WlanHostedNetworkRefreshSecuritySettings function
author: windows-sdk-content
description: Refreshes the configurable and auto-generated parts of the wireless Hosted Network security settings.
old-location: nwifi\wlanhostednetworkrefreshsecuritysettings.htm
old-project: NativeWiFi
ms.assetid: 9589e3a6-6e7a-4186-bfd0-a942a39ecafb
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: WlanHostedNetworkRefreshSecuritySettings, WlanHostedNetworkRefreshSecuritySettings function [NativeWIFI], nwifi.wlanhostednetworkrefreshsecuritysettings, wlanapi/WlanHostedNetworkRefreshSecuritySettings
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wlanapi.dll
api_name:
-	WlanHostedNetworkRefreshSecuritySettings
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanHostedNetworkRefreshSecuritySettings function


## -description


The <b>WlanHostedNetworkRefreshSecuritySettings</b> function refreshes the configurable and auto-generated parts of the wireless Hosted Network security settings. 


## -parameters




### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <b>WlanHostedNetworkRefreshSecuritySettings</b> function fails. Possible values for the failure reason are from the <a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i>header file.


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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -remarks



The <b>WlanHostedNetworkRefreshSecuritySettings</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkRefreshSecuritySettings</b> function to force a refresh of the configurable and auto-generated parts of the security settings (the primary key) on the wireless Hosted Network. 

An application might call the <b>WlanHostedNetworkRefreshSecuritySettings</b> function after ensuring that the user accepts the impact of updating the security settings. In order to succeed,  this function must persist the new settings which would require that Hosted Network state be transitioned to wlan_hosted_network_idle if it was currently running (wlan_hosted_network_active). 

<div class="alert"><b>Note</b>  Any network clients (PCs or devices) on the wireless Hosted Network would have to be re-configured after calling the <b>WlanHostedNetworkRefreshSecuritySettings</b> function if their continued usage is a goal. An application would typically call this function in situations where the user feels that the security of the previous primary key used for security by the wireless Hosted Network has been violated. Note that the <b>WlanHostedNetworkRefreshSecuritySettings</b> function does not change or reset the secondary key.</div>
<div> </div>
Any Hosted Network state change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


Any user can call the <b>WlanHostedNetworkRefreshSecuritySettings</b> function to refresh the security settings on the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/56e86ef8-f759-4e56-a591-74e03430125a">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a>



<a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/aed4db5d-9740-43ee-bf09-7a4a5abae953">WlanHostedNetworkInitSettings</a>



<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>



<a href="https://msdn.microsoft.com/9589e3a6-6e7a-4186-bfd0-a942a39ecafb">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a>



<a href="https://msdn.microsoft.com/385148fd-b5cd-4221-be25-077f484e93e9">WlanHostedNetworkSetSecondaryKey</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>
 

 

