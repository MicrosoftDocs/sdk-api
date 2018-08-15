---
UID: NF:wlanapi.WlanHostedNetworkQuerySecondaryKey
title: WlanHostedNetworkQuerySecondaryKey function
author: windows-sdk-content
description: Queries the secondary security key that is configured to be used by the wireless Hosted Network.
old-location: nwifi\wlanhostednetworkquerysecondarykey.htm
old-project: nativewifi
ms.assetid: 5989977a-7a2f-43b8-a958-058db01fd24f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WlanHostedNetworkQuerySecondaryKey, WlanHostedNetworkQuerySecondaryKey function [NativeWIFI], nwifi.wlanhostednetworkquerysecondarykey, wlanapi/WlanHostedNetworkQuerySecondaryKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.redist: 
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
tech.root: 
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanHostedNetworkQuerySecondaryKey
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanHostedNetworkQuerySecondaryKey function


## -description


The <b>WlanHostedNetworkQuerySecondaryKey</b> function queries the secondary security key that is configured to be used by the wireless Hosted Network. 


## -parameters




### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


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

An optional pointer to a value that receives the failure reason,  if the call to the <a href="https://msdn.microsoft.com/385148fd-b5cd-4221-be25-077f484e93e9">WlanHostedNetworkSetSecondaryKey</a> function fails. Possible values for the failure reason are from the <a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a> enumeration type defined in the <i>Wlanapi.h </i>header file.


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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -remarks



The <b>WlanHostedNetworkQuerySecondaryKey</b> function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanHostedNetworkQuerySecondaryKey</b> function to query the secondary security key that will be used by the wireless Hosted Network. This function will return the key information including key data, key length, whether it is a passphrase, and whether it is persistent or for one-time use. This function does not change the state or properties of the wireless Hosted Network.

The secondary security key is a passphrase if the value pointed to by the <i>pbIsPassPhrase</i> parameter is <b>TRUE</b>.  The secondary security key is a binary key if the value pointed to by the <i>pbIsPassPhrase</i> parameter is <b>FALSE</b>.  

The secondary security key returned in the buffer pointed to by the <i>ppucKeyData</i> parameter is used with WPA2-Personal authentication and is in one of the following formats:<ul>
<li>A key passphrase that consists of an array of ASCII characters from 8 to 63 characters. The value pointed to by the <i>pdwKeyLength</i> parameter includes the terminating ‘\0’ in the passphrase. The value pointed to by the <i>pdwKeyLength</i> parameter should be in the range of 9 to 64. </li>
<li>A	binary key that conists of 32 bytes of binary key data. The value pointed to by the <i>pdwKeyLength</i> parameter should be 32 for binary key.</li>
</ul>


The secondary security key is persistent if the value pointed to by the <i>pbPersistent</i> parameter is <b>TRUE</b>. When persistent, the secondary security key would  be used immediately if the Hosted Network is already started, and also reused whenever Hosted Network is started in the future. 

If secondary security key is not specified as persistent, it will be used immediately if the Hosted Network is already started, or only for the next time when the Hosted Network is started. After the Hosted Network is stopped, this secondary security key will never be used again and will be removed from the system.

If there is no secondary security key currently configured, the returned value pointed to by the <i>pdwKeyLength</i> parameter will be zero, and the value returned in the <i>ppucKeyData</i> parameter will be <b>NULL</b>. In such case, the value returned in the <i>pbIsPassPhrase</i> and <i>pbPersistent</i> parameters will be meaningless.

If the <b>WlanHostedNetworkQuerySecondaryKey</b> function succeeds, the memory used for the buffer in the <i>ppucKeyData</i> parameter that is returned should be freed after use by calling the <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function.

Any user can call the <b>WlanHostedNetworkQuerySecondaryKey</b> function to query the secondary security key used in the Hosted Network. However, the ability to enable the wireless Hosted Network may be restricted by group policy in a domain.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/56e86ef8-f759-4e56-a591-74e03430125a">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="https://msdn.microsoft.com/affca9ab-fcd4-474d-993c-f6bb6b1f967c">WLAN_HOSTED_NETWORK_REASON</a>



<a href="https://msdn.microsoft.com/8e944133-2616-4e17-ac38-c17e8d25ccec">WlanCloseHandle</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>



<a href="https://msdn.microsoft.com/aed4db5d-9740-43ee-bf09-7a4a5abae953">WlanHostedNetworkInitSettings</a>



<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>



<a href="https://msdn.microsoft.com/9589e3a6-6e7a-4186-bfd0-a942a39ecafb">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a>



<a href="https://msdn.microsoft.com/385148fd-b5cd-4221-be25-077f484e93e9">WlanHostedNetworkSetSecondaryKey</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>
 

 

