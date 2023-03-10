---
UID: NS:wlanapi._WLAN_AVAILABLE_NETWORK
title: WLAN_AVAILABLE_NETWORK (wlanapi.h)
description: Contains information about an available wireless network. (WLAN_AVAILABLE_NETWORK)
helpviewer_keywords: ["*PWLAN_AVAILABLE_NETWORK","PWLAN_AVAILABLE_NETWORK","PWLAN_AVAILABLE_NETWORK structure pointer [NativeWIFI]","WLAN_AVAILABLE_NETWORK","WLAN_AVAILABLE_NETWORK structure [NativeWIFI]","WLAN_AVAILABLE_NETWORK_CONNECTED","WLAN_AVAILABLE_NETWORK_HAS_PROFILE","dot11_phy_type_IHV_end","dot11_phy_type_IHV_start","dot11_phy_type_any","dot11_phy_type_dsss","dot11_phy_type_erp","dot11_phy_type_fhss","dot11_phy_type_hrdsss","dot11_phy_type_ht","dot11_phy_type_irbaseband","dot11_phy_type_ofdm","dot11_phy_type_unknown","dot11_phy_type_vht","nativewifi.wlan_visible_network","nwifi.wlan_available_network","wlanapi/PWLAN_AVAILABLE_NETWORK","wlanapi/WLAN_AVAILABLE_NETWORK"]
old-location: nwifi\wlan_available_network.htm
tech.root: nwifi
ms.assetid: 82883cea-515b-426d-9961-c144ce99b3db
ms.date: 12/05/2018
ms.keywords: '*PWLAN_AVAILABLE_NETWORK, PWLAN_AVAILABLE_NETWORK, PWLAN_AVAILABLE_NETWORK structure pointer [NativeWIFI], WLAN_AVAILABLE_NETWORK, WLAN_AVAILABLE_NETWORK structure [NativeWIFI], WLAN_AVAILABLE_NETWORK_CONNECTED, WLAN_AVAILABLE_NETWORK_HAS_PROFILE, dot11_phy_type_IHV_end, dot11_phy_type_IHV_start, dot11_phy_type_any, dot11_phy_type_dsss, dot11_phy_type_erp, dot11_phy_type_fhss, dot11_phy_type_hrdsss, dot11_phy_type_ht, dot11_phy_type_irbaseband, dot11_phy_type_ofdm, dot11_phy_type_unknown, dot11_phy_type_vht, nativewifi.wlan_visible_network, nwifi.wlan_available_network, wlanapi/PWLAN_AVAILABLE_NETWORK, wlanapi/WLAN_AVAILABLE_NETWORK'
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
req.typenames: WLAN_AVAILABLE_NETWORK, *PWLAN_AVAILABLE_NETWORK
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_AVAILABLE_NETWORK
 - wlanapi/_WLAN_AVAILABLE_NETWORK
 - PWLAN_AVAILABLE_NETWORK
 - wlanapi/PWLAN_AVAILABLE_NETWORK
 - WLAN_AVAILABLE_NETWORK
 - wlanapi/WLAN_AVAILABLE_NETWORK
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
 - WLAN_AVAILABLE_NETWORK
---

# WLAN_AVAILABLE_NETWORK structure


## -description

The <b>WLAN_AVAILABLE_NETWORK</b> structure contains information about an available wireless network.

## -struct-fields

### -field strProfileName

Contains the profile name associated with the network.  If the network does not have a profile, this member will be empty.  If multiple profiles are associated with the network, there will be multiple entries with the same SSID in the visible network list. Profile names are case-sensitive. This string must be NULL-terminated.

### -field dot11Ssid

A <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that contains the SSID of the visible wireless network.

### -field dot11BssType

A <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> value that specifies whether the network is infrastructure or ad hoc.

### -field uNumberOfBssids

Indicates the number of BSSIDs in the network.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><b>uNumberofBssids</b> is at most 1, regardless of the number of access points broadcasting the SSID.

### -field bNetworkConnectable

Indicates whether the network is connectable or not.    If set to <b>TRUE</b>, the network is connectable, otherwise the network cannot be connected to.

### -field wlanNotConnectableReason

A WLAN_REASON_CODE value that indicates why a network cannot be connected to.  This member is only valid when  <b>bNetworkConnectable</b> is <b>FALSE</b>.

### -field uNumberOfPhyTypes

The number of PHY types supported on available networks. The maximum value of <i>uNumberOfPhyTypes</i> is <b>WLAN_MAX_PHY_TYPE_NUMBER</b>, which has a value of 8. If more than <b>WLAN_MAX_PHY_TYPE_NUMBER</b> PHY types are supported, <i>bMorePhyTypes</i> must be set to <b>TRUE</b>.

### -field dot11PhyTypes

Contains an array of <a href="/windows/desktop/NativeWiFi/dot11-phy-type">DOT11_PHY_TYPE</a> values that represent the PHY types supported by the available networks. When <i>uNumberOfPhyTypes</i> is greater than <b>WLAN_MAX_PHY_TYPE_NUMBER</b>, this array contains only the first <b>WLAN_MAX_PHY_TYPE_NUMBER</b> PHY types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_unknown"></a><a id="DOT11_PHY_TYPE_UNKNOWN"></a><dl>
<dt><b>dot11_phy_type_unknown</b></dt>
</dl>
</td>
<td width="60%">
Specifies an unknown or uninitialized PHY type. 

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_any"></a><a id="DOT11_PHY_TYPE_ANY"></a><dl>
<dt><b>dot11_phy_type_any</b></dt>
</dl>
</td>
<td width="60%">
Specifies any PHY type.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_fhss"></a><a id="DOT11_PHY_TYPE_FHSS"></a><dl>
<dt><b>dot11_phy_type_fhss</b></dt>
</dl>
</td>
<td width="60%">
Specifies a frequency-hopping spread-spectrum (FHSS) PHY. Bluetooth devices can use FHSS or an adaptation of FHSS.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_dsss"></a><a id="DOT11_PHY_TYPE_DSSS"></a><dl>
<dt><b>dot11_phy_type_dsss</b></dt>
</dl>
</td>
<td width="60%">
Specifies a direct sequence spread spectrum (DSSS) PHY. 

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_irbaseband"></a><a id="DOT11_PHY_TYPE_IRBASEBAND"></a><dl>
<dt><b>dot11_phy_type_irbaseband</b></dt>
</dl>
</td>
<td width="60%">
Specifies an infrared (IR) baseband PHY. 

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_ofdm"></a><a id="DOT11_PHY_TYPE_OFDM"></a><dl>
<dt><b>dot11_phy_type_ofdm</b></dt>
</dl>
</td>
<td width="60%">
Specifies an orthogonal frequency division multiplexing (OFDM) PHY.  802.11a devices can use OFDM.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_hrdsss"></a><a id="DOT11_PHY_TYPE_HRDSSS"></a><dl>
<dt><b>dot11_phy_type_hrdsss</b></dt>
</dl>
</td>
<td width="60%">
Specifies a high-rate DSSS (HRDSSS) PHY.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_erp"></a><a id="DOT11_PHY_TYPE_ERP"></a><dl>
<dt><b>dot11_phy_type_erp</b></dt>
</dl>
</td>
<td width="60%">
Specifies an extended rate PHY (ERP). 802.11g devices can use ERP.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_ht"></a><a id="DOT11_PHY_TYPE_HT"></a><dl>
<dt><b>dot11_phy_type_ht</b></dt>
</dl>
</td>
<td width="60%">
Specifies an 802.11n PHY type.



</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_vht"></a><a id="DOT11_PHY_TYPE_VHT"></a><dl>
<dt><b>dot11_phy_type_vht</b></dt>
</dl>
</td>
<td width="60%">
Specifies the 802.11ac PHY type. This is the very high throughput PHY type specified in IEEE 802.11ac.

This value is supported on Windows 8.1, Windows Server 2012 R2, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_IHV_start"></a><a id="dot11_phy_type_ihv_start"></a><a id="DOT11_PHY_TYPE_IHV_START"></a><dl>
<dt><b>dot11_phy_type_IHV_start</b></dt>
</dl>
</td>
<td width="60%">
Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_phy_type_IHV_end"></a><a id="dot11_phy_type_ihv_end"></a><a id="DOT11_PHY_TYPE_IHV_END"></a><dl>
<dt><b>dot11_phy_type_IHV_end</b></dt>
</dl>
</td>
<td width="60%">
Specifies the end of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).

</td>
</tr>
</table>

### -field bMorePhyTypes

Specifies if there are more than <b>WLAN_MAX_PHY_TYPE_NUMBER</b> PHY types supported. 

When this member is set to <b>TRUE</b>, an application must call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a> to get the complete list of PHY types. The returned  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> structure has an array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a> structures. The <i>uPhyId</i> member of the <b>WLAN_BSS_ENTRY</b>   structure contains the PHY type for an entry.

### -field wlanSignalQuality

A percentage value that represents the signal quality of the network.  <b>WLAN_SIGNAL_QUALITY</b> is of type <b>ULONG</b>.  This member contains a value between 0 and 100. A value of 0 implies an actual RSSI signal strength of -100 dbm. A value of 100 implies an actual RSSI signal strength of -50 dbm. You can calculate the RSSI signal strength value for <b>wlanSignalQuality</b> values between 1 and 99 using linear interpolation.

### -field bSecurityEnabled

Indicates whether security is enabled on the network.  A value of <b>TRUE</b> indicates that security is enabled, otherwise it is not.

### -field dot11DefaultAuthAlgorithm

A <a href="/windows/desktop/NativeWiFi/dot11-auth-algorithm">DOT11_AUTH_ALGORITHM</a> value that indicates the default authentication algorithm used to join this network for the first time.

### -field dot11DefaultCipherAlgorithm

A <a href="/windows/desktop/NativeWiFi/dot11-cipher-algorithm">DOT11_CIPHER_ALGORITHM</a> value that indicates the default cipher algorithm to be used when joining this network.

### -field dwFlags

Contains various flags for the network.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_AVAILABLE_NETWORK_CONNECTED"></a><a id="wlan_available_network_connected"></a><dl>
<dt><b>WLAN_AVAILABLE_NETWORK_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
This network is currently connected.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_AVAILABLE_NETWORK_HAS_PROFILE"></a><a id="wlan_available_network_has_profile"></a><dl>
<dt><b>WLAN_AVAILABLE_NETWORK_HAS_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
There is a profile for this network.

</td>
</tr>
</table>

### -field dwReserved

Reserved for future use.  Must be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a>
