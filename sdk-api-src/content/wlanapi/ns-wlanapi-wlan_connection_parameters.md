---
UID: NS:wlanapi._WLAN_CONNECTION_PARAMETERS
title: WLAN_CONNECTION_PARAMETERS (wlanapi.h)
description: Specifies the parameters used when using the WlanConnect function.
helpviewer_keywords: ["*PWLAN_CONNECTION_PARAMETERS","PWLAN_CONNECTION_PARAMETERS","PWLAN_CONNECTION_PARAMETERS structure pointer [NativeWIFI]","WLAN_CONNECTION_PARAMETERS","WLAN_CONNECTION_PARAMETERS structure [NativeWIFI]","nwifi.wlan_connection_parameters","wlanapi/PWLAN_CONNECTION_PARAMETERS","wlanapi/WLAN_CONNECTION_PARAMETERS"]
old-location: nwifi\wlan_connection_parameters.htm
tech.root: nwifi
ms.assetid: e0321447-b89a-4f4e-929e-eb6db76f7283
ms.date: 12/05/2018
ms.keywords: '*PWLAN_CONNECTION_PARAMETERS, PWLAN_CONNECTION_PARAMETERS, PWLAN_CONNECTION_PARAMETERS structure pointer [NativeWIFI], WLAN_CONNECTION_PARAMETERS, WLAN_CONNECTION_PARAMETERS structure [NativeWIFI], nwifi.wlan_connection_parameters, wlanapi/PWLAN_CONNECTION_PARAMETERS, wlanapi/WLAN_CONNECTION_PARAMETERS'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WLAN_CONNECTION_PARAMETERS, *PWLAN_CONNECTION_PARAMETERS
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_CONNECTION_PARAMETERS
 - wlanapi/_WLAN_CONNECTION_PARAMETERS
 - PWLAN_CONNECTION_PARAMETERS
 - wlanapi/PWLAN_CONNECTION_PARAMETERS
 - WLAN_CONNECTION_PARAMETERS
 - wlanapi/WLAN_CONNECTION_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_CONNECTION_PARAMETERS
---

# WLAN_CONNECTION_PARAMETERS structure


## -description

The <b>WLAN_CONNECTION_PARAMETERS</b> structure specifies the parameters used when using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a> function.

## -struct-fields

### -field wlanConnectionMode

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_connection_mode">WLAN_CONNECTION_MODE</a> value that specifies the mode of connection.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.

### -field strProfile.string

### -field strProfile

Specifies the profile being used for the connection. 

If  <b>wlanConnectionMode</b> is set to <b>wlan_connection_mode_profile</b>, then <b>strProfile</b> specifies the name of the profile used for the connection. If <b>wlanConnectionMode</b> is set to <b>wlan_connection_mode_temporary_profile</b>, then <b>strProfile</b> specifies the XML representation of the profile used for the connection. If <b>wlanConnectionMode</b> is set to <b>wlan_connection_mode_discovery_secure</b> or <b>wlan_connection_mode_discovery_unsecure</b>, then <b>strProfile</b> should be set to <b>NULL</b>.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The profile must meet the compatibility criteria described in <a href="/windows/desktop/NativeWiFi/wireless-profile-compatibility">Wireless Profile Compatibility</a>.

### -field pDot11Ssid

Pointer to a <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that specifies the SSID of the network to connect to.  This parameter is optional. When set to <b>NULL</b>, all SSIDs in the profile will be tried.  This parameter must not be <b>NULL</b> if <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_connection_mode">WLAN_CONNECTION_MODE</a> is set to <b>wlan_connection_mode_discovery_secure</b> or <b>wlan_connection_mode_discovery_unsecure</b>.

### -field pDesiredBssidList

Pointer to a <a href="/windows/desktop/NativeWiFi/dot11-bssid-list">DOT11_BSSID_LIST</a> structure that contains the list of basic service set (BSS) identifiers desired for the connection.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This member must be <b>NULL</b>.

### -field dot11BssType

A <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> value that indicates the BSS type of the network.  If a profile is provided, this BSS type must be the same as the one in the profile.

### -field dwFlags

The following table shows flags used to specify the connection parameters.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WLAN_CONNECTION_HIDDEN_NETWORK</td>
<td>0x00000001</td>
<td>Connect to the destination network even if the destination is a hidden network. A hidden network does not broadcast its SSID. Do not use this flag if the destination network is an ad-hoc network.If the profile specified by <b>strProfile</b> is not <b>NULL</b>, then this flag is ignored and the <a href="/windows/win32/nativewifi/wlan-profileschema-ssidconfig-wlanprofile-element#nonbroadcast">nonBroadcast</a> profile element determines whether to connect to a hidden network.

</td>
</tr>
<tr>
<td>WLAN_CONNECTION_ADHOC_JOIN_ONLY</td>
<td>0x00000002</td>
<td>Do not form an ad-hoc network. Only join an ad-hoc network if the network already exists. Do not use this flag if the destination network is an infrastructure network.</td>
</tr>
<tr>
<td>WLAN_CONNECTION_IGNORE_PRIVACY_BIT</td>
<td>0x00000004</td>
<td>Ignore the privacy bit when connecting to the network. Ignoring the privacy bit has the effect of ignoring whether packets are encrypted and ignoring the method of encryption used. Only use this flag when connecting to an infrastructure network using a temporary profile.</td>
</tr>
<tr>
<td>WLAN_CONNECTION_EAPOL_PASSTHROUGH </td>
<td>0x00000008</td>
<td>Exempt EAPOL traffic from encryption and decryption. This flag is used when an application must send EAPOL traffic over an infrastructure  network that uses Open authentication and WEP encryption. This flag must not be used to connect to networks that require 802.1X authentication. This flag is only valid when <b>wlanConnectionMode</b> is set to <b>wlan_connection_mode_temporary_profile</b>. Avoid using this flag whenever possible.</td>
</tr>
<tr>
<td>WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE </td>
<td>0x00000010</td>
<td>Automatically persist discovery profile on successful connection completion.
This flag is only valid for wlan_connection_mode_discovery_secure or
wlan_connection_mode_discovery_unsecure. The profile will be saved as an all 
user profile, with the name generated from the SSID using WlanUtf8SsidToDisplayName. 
If there is already a profile with the same name, a number will be appended 
to the end of the profile name. The profile will be saved with manual connection mode,
unless WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE_CONNECTION_MODE_AUTO is also specified.</td>
</tr>
<tr>
<td>WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE_CONNECTION_MODE_AUTO </td>
<td>0x00000020</td>
<td>To be used in conjunction with WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE. The 
discovery profile will be persisted with automatic connection mode.</td>
</tr>
<tr>
<td>WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE_OVERWRITE_EXISTING</td>
<td>0x00000040</td>
<td>To be used in conjunction with WLAN_CONNECTION_PERSIST_DISCOVERY_PROFILE. The 
discovery profile will be persisted and attempt to overwrite an existing profile with the same name.</td>
</tr>
</table>
 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This member must be set to 0.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a>