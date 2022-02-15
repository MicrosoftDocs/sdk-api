---
UID: NF:wlanapi.WlanHostedNetworkQuerySecondaryKey
title: WlanHostedNetworkQuerySecondaryKey function (wlanapi.h)
description: Queries the secondary security key that is configured to be used by the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkQuerySecondaryKey","WlanHostedNetworkQuerySecondaryKey function [NativeWIFI]","nwifi.wlanhostednetworkquerysecondarykey","wlanapi/WlanHostedNetworkQuerySecondaryKey"]
old-location: nwifi\wlanhostednetworkquerysecondarykey.htm
tech.root: nwifi
ms.assetid: 5989977a-7a2f-43b8-a958-058db01fd24f
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkQuerySecondaryKey, WlanHostedNetworkQuerySecondaryKey function [NativeWIFI], nwifi.wlanhostednetworkquerysecondarykey, wlanapi/WlanHostedNetworkQuerySecondaryKey
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
 - WlanHostedNetworkQuerySecondaryKey
 - wlanapi/WlanHostedNetworkQuerySecondaryKey
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
 - WlanHostedNetworkQuerySecondaryKey
---

# WlanHostedNetworkQuerySecondaryKey function


## -description

The <b>WlanHostedNetworkQuerySecondaryKey</b> function queries the secondary security key that is configured to be used by the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pdwKeyLength [out]

A pointer to a value that specifies number of valid data bytes in the key data array pointed to by the <i>ppucKeyData</i> parameter, if the call to the <b>WlanHostedNetworkQuerySecondaryKey</b> function succeeds. 

This key length includes the terminating ‘\0’ if the key is a passphrase.

### -param ppucKeyData [out]

A pointer to a value that receives a pointer to the buffer returned with the secondary security key data,  if the call to the <b>WlanHostedNetworkQuerySecondaryKey</b> function succeeds.

### -param pbIsPassPhrase [out]

A pointer to a Boolean value that indicates if the key data array pointed to by the <i>ppucKeyData</i> parameter is in passphrase format. 

If this parameter is <b>TRUE</b>, the key data array is in passphrase format. If this parameter is <b>FALSE</b>, the key data array is not in passphrase format.

### -param pbPersistent [out]

A pointer to a Boolean value that indicates if the key data array pointed to by the <i>ppucKeyData</i> parameter is to be stored and reused later or is for one-time use only. 

If this parameter is <b>TRUE</b>, the key data array is to be stored and reused later. If this parameter is <b>FALSE</b>, the key data array is for one-time use only.

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey">WlanHostedNetworkSetSecondaryKey</a> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
<li><i>pdwKeyLength</i> is <b>NULL</b>.</li>
<li><i>ppucKeyData</i> is <b>NULL</b> or invalid.</li>
<li><i>pbIsPassPhrase</i> is <b>NULL</b> or invalid.</li>
<li><i>pbPersistent</i> is <b>NULL</b>.</li>
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

The <b>WlanHostedNetworkQuerySecondaryKey</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkQuerySecondaryKey</b> function to query the secondary security key that will be used by the wireless Hosted Network. This function will return the key information including key data, key length, whether it is a passphrase, and whether it is persistent or for one-time use. This function does not change the state or properties of the wireless Hosted Network.

The secondary security key is a passphrase if the value pointed to by the <i>pbIsPassPhrase</i> parameter is <b>TRUE</b>.  The secondary security key is a binary key if the value pointed to by the <i>pbIsPassPhrase</i> parameter is <b>FALSE</b>.  

The secondary security key returned in the buffer pointed to by the <i>ppucKeyData</i> parameter is used with WPA2-Personal authentication and is in one of the following formats:<ul>
<li>A key passphrase that consists of an array of ASCII characters from 8 to 63 characters. The value pointed to by the <i>pdwKeyLength</i> parameter includes the terminating ‘\0’ in the passphrase. The value pointed to by the <i>pdwKeyLength</i> parameter should be in the range of 9 to 64. </li>
<li>A binary key that consists of 32 bytes of binary key data. The value pointed to by the <i>pdwKeyLength</i> parameter should be 32 for binary key.</li>
</ul>


The secondary security key is persistent if the value pointed to by the <i>pbPersistent</i> parameter is <b>TRUE</b>. When persistent, the secondary security key would  be used immediately if the Hosted Network is already started, and also reused whenever Hosted Network is started in the future. 

If secondary security key is not specified as persistent, it will be used immediately if the Hosted Network is already started, or only for the next time when the Hosted Network is started. After the Hosted Network is stopped, this secondary security key will never be used again and will be removed from the system.

If there is no secondary security key currently configured, the returned value pointed to by the <i>pdwKeyLength</i> parameter will be zero, and the value returned in the <i>ppucKeyData</i> parameter will be <b>NULL</b>. In such case, the value returned in the <i>pbIsPassPhrase</i> and <i>pbPersistent</i> parameters will be meaningless.

If the <b>WlanHostedNetworkQuerySecondaryKey</b> function succeeds, the memory used for the buffer in the <i>ppucKeyData</i> parameter that is returned should be freed after use by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function.

Any user can call the <b>WlanHostedNetworkQuerySecondaryKey</b> function to query the secondary security key used in the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkinitsettings">WlanHostedNetworkInitSettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerystatus">WlanHostedNetworkQueryStatus</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey">WlanHostedNetworkSetSecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>