---
UID: NF:wlanapi.WlanHostedNetworkSetSecondaryKey
title: WlanHostedNetworkSetSecondaryKey function (wlanapi.h)
description: Configures the secondary security key that will be used by the wireless Hosted Network.
helpviewer_keywords: ["WlanHostedNetworkSetSecondaryKey","WlanHostedNetworkSetSecondaryKey function [NativeWIFI]","nwifi.wlanhostednetworksetsecondarykey","wlanapi/WlanHostedNetworkSetSecondaryKey"]
old-location: nwifi\wlanhostednetworksetsecondarykey.htm
tech.root: nwifi
ms.assetid: 385148fd-b5cd-4221-be25-077f484e93e9
ms.date: 12/05/2018
ms.keywords: WlanHostedNetworkSetSecondaryKey, WlanHostedNetworkSetSecondaryKey function [NativeWIFI], nwifi.wlanhostednetworksetsecondarykey, wlanapi/WlanHostedNetworkSetSecondaryKey
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
 - WlanHostedNetworkSetSecondaryKey
 - wlanapi/WlanHostedNetworkSetSecondaryKey
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
 - WlanHostedNetworkSetSecondaryKey
---

# WlanHostedNetworkSetSecondaryKey function


## -description

The <b>WlanHostedNetworkSetSecondaryKey</b> function configures the secondary security key that will be used by the wireless Hosted Network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param dwKeyLength [in]

The number of valid data bytes in the key data array pointed to by the <i>pucKeyData</i> parameter. This key length should include the terminating ‘\0’ if the key is a passphrase.

### -param pucKeyData [in]

A pointer to a buffer that contains the key data. The number of valid data bytes in the buffer must be at least the value specified in <i>dwKeyLength</i> parameter.

### -param bIsPassPhrase [in]

A Boolean value that indicates if the key data array pointed to by the <i>pucKeyData</i> parameter is in passphrase format. 

If this parameter is <b>TRUE</b>, the key data array is in passphrase format. If this parameter is <b>FALSE</b>, the key data array is not in passphrase format.

### -param bPersistent [in]

A Boolean value that indicates if the key data array pointed to by the <i>pucKeyData</i> parameter is to be stored and reused later or is for one-time use only. 

If this parameter is <b>TRUE</b>, the key data array is to be stored and reused later. If this parameter is <b>FALSE</b>, the key data array is to be used for one session (either the current session or the next session if the Hosted Network is not started).

### -param pFailReason [out, optional]

An optional pointer to a value that receives the failure reason,  if the call to the <b>WlanHostedNetworkSetSecondaryKey</b> function fails. Possible values for the failure reason are from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i> header file.

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
<li><i>pucKeyData</i> is <b>NULL</b>.</li>
<li><i>pucKeyData</i> does not point to a well- formed valid key.</li>
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

The <b>WlanHostedNetworkSetSecondaryKey</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkSetSecondaryKey</b> function to configure the secondary security key that will be used by the wireless Hosted Network. 
Any Hosted Network change caused by this function would not be automatically undone if the calling application closes its calling handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


Once started, the wireless Hosted Network will allow wireless peers to associate with this secondary security key in addition to the primary security key. The secondary security key is always specified by the user as needed, while the primary security key is generated by the operating system with greater security strength.

The secondary security key passed in the buffer pointed to by the <i>pucKeyData</i> parameter is used with WPA2-Personal authentication and should be in one of the following formats:<ul>
<li>A key passphrase that consists of an array of ASCII characters from 8 to 63 characters. The <i>dwKeyLength</i> parameter should include the terminating ‘\0’ in the passphrase. The value of the <i>dwKeyLength</i> parameter should be in the range of 9 to 64. </li>
<li>A	binary key that consists of 32 bytes of binary key data. The <i>dwKeyLength</i> parameter should be 32 for binary key.</li>
</ul>


To configure a valid secondary security key, the <i>dwKeyLength</i> parameter should be in the correct range and the <i>pucKeyData</i> parameter should point to a valid memory buffer containing the specified bytes of data. To remove the currently configured secondary security key from the system, the application should call the <b>WlanHostedNetworkSetSecondaryKey</b> function with zero in <i>dwKeyLength</i> parameter and <b>NULL</b> in the <i>pucKeyData</i> parameter. 

The <b>WlanHostedNetworkSetSecondaryKey</b> function will return <b>ERROR_INVALID_PARAMETER</b> if the <i>pucKeyData</i> parameter is <b>NULL</b>, but the <i>dwKeyLength</i> parameter  is not zero.  The <b>WlanHostedNetworkSetSecondaryKey</b> function will also return <b>ERROR_INVALID_PARAMETER</b> if the <i>dwKeyLength</i> parameter  is zero, but <i>pucKeyData</i> parameter  is not <b>NULL</b>.

The secondary security key is usually set before the wireless Hosted Network is started. Then it will be used the next time when the Hosted Network is started. 

A secondary security key can also be set after the Hosted Network has been started. In this case, the secondary security key will be used immediately. Any clients using the previous secondary security key will remain connected, but they will be unable to reconnect if they get disconnected for any reason or if the wireless Hosted Network is restarted.

The secondary security key can be specified as persistent if the <i>bPersistent</i> parameter is set to <b>TRUE</b>. When specified as persistent, the secondary security key would  be used immediately if the Hosted Network is already started, and also reused whenever Hosted Network is started in the future. 

If secondary security key is not specified as persistent, it will be used immediately if the Hosted Network is already started, or only for the next time when Hosted Network is started. After the Hosted Network is stopped, this secondary security key will never be used again and will be removed from the system.

Any user can call this function to configure the secondary security key to be used in the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_hosted_network_reason">WLAN_HOSTED_NETWORK_REASON</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkinitsettings">WlanHostedNetworkInitSettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty">WlanHostedNetworkQueryProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey">WlanHostedNetworkQuerySecondaryKey</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanhostednetworksetproperty">WlanHostedNetworkSetProperty</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>