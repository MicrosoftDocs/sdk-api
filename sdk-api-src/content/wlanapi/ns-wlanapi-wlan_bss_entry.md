---
UID: NS:wlanapi._WLAN_BSS_ENTRY
title: WLAN_BSS_ENTRY (wlanapi.h)
description: Contains information about a basic service set (BSS).
helpviewer_keywords: ["*PWLAN_BSS_ENTRY","CF Poll Request","CF-Pollable","ESS","IBSS","PWLAN_BSS_ENTRY","PWLAN_BSS_ENTRY structure pointer [NativeWIFI]","Privacy","WLAN_BSS_ENTRY","WLAN_BSS_ENTRY structure [NativeWIFI]","dot11_BSS_type_independent","dot11_BSS_type_infrastructure","nwifi.wlan_bss_entry","wlanapi/PWLAN_BSS_ENTRY","wlanapi/WLAN_BSS_ENTRY"]
old-location: nwifi\wlan_bss_entry.htm
tech.root: nwifi
ms.assetid: 25a76128-13d9-47dd-9c73-1fbf06a908be
ms.date: 12/05/2018
ms.keywords: '*PWLAN_BSS_ENTRY, CF Poll Request, CF-Pollable, ESS, IBSS, PWLAN_BSS_ENTRY, PWLAN_BSS_ENTRY structure pointer [NativeWIFI], Privacy, WLAN_BSS_ENTRY, WLAN_BSS_ENTRY structure [NativeWIFI], dot11_BSS_type_independent, dot11_BSS_type_infrastructure, nwifi.wlan_bss_entry, wlanapi/PWLAN_BSS_ENTRY, wlanapi/WLAN_BSS_ENTRY'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: WLAN_BSS_ENTRY, *PWLAN_BSS_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_BSS_ENTRY
 - wlanapi/_WLAN_BSS_ENTRY
 - PWLAN_BSS_ENTRY
 - wlanapi/PWLAN_BSS_ENTRY
 - WLAN_BSS_ENTRY
 - wlanapi/WLAN_BSS_ENTRY
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
 - WLAN_BSS_ENTRY
---

# WLAN_BSS_ENTRY structure


## -description

The <b>WLAN_BSS_ENTRY</b> structure contains information about a basic service set (BSS).

## -struct-fields

### -field dot11Ssid

The SSID of the access point (AP) or peer station associated with the BSS. The data type for this member is a <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure.

### -field uPhyId

The identifier (ID) of the PHY that the wireless LAN interface used to detect the BSS network.

### -field dot11Bssid

The media access control (MAC) address of the access point for infrastructure BSS networks or the peer station for independent BSS networks (ad hoc networks) that sent the 802.11 Beacon or Probe Response frame received by the wireless LAN interface while scanning. The data type for this member is a <a href="/windows/desktop/NativeWiFi/dot11-mac-address-type">DOT11_MAC_ADDRESS</a> structure.

### -field dot11BssType

The BSS network type. The data type for this member is a <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> enumeration value.   

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dot11_BSS_type_infrastructure"></a><a id="dot11_bss_type_infrastructure"></a><a id="DOT11_BSS_TYPE_INFRASTRUCTURE"></a><dl>
<dt><b>dot11_BSS_type_infrastructure</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies an infrastructure BSS network.



</td>
</tr>
<tr>
<td width="40%"><a id="dot11_BSS_type_independent"></a><a id="dot11_bss_type_independent"></a><a id="DOT11_BSS_TYPE_INDEPENDENT"></a><dl>
<dt><b>dot11_BSS_type_independent</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Specifies an independent BSS (IBSS) network (an ad hoc network).



</td>
</tr>
</table>

### -field dot11BssPhyType

The PHY type for this network. The data type for this member is a <a href="/windows/desktop/NativeWiFi/dot11-phy-type">DOT11_PHY_TYPE</a> enumeration value.

### -field lRssi

The received signal strength indicator (RSSI) value, in units of decibels referenced to 1.0 milliwatts (dBm), as detected by the wireless LAN interface driver for the AP or peer station.

### -field uLinkQuality

The link quality reported by the wireless LAN interface driver. The link quality value ranges from 0 through 100. A value of 100 specifies the highest link quality.

### -field bInRegDomain

A value that specifies whether the AP or peer station is operating within the regulatory domain as identified by the country/region.

If the wireless LAN interface driver does not support multiple regulatory domains, this member is set to <b>TRUE</b>.

If the 802.11 Beacon or Probe Response frame received from the AP or peer station does not include a Country information element (IE), this member is set to <b>TRUE</b>. 

If the 802.11 Beacon or Probe Response frame received from the AP or peer station does include a Country IE, this member is set to <b>FALSE</b> if the value of the Country String subfield does not equal the input country string.

### -field usBeaconPeriod

The value of the Beacon Interval field from the 802.11 Beacon or Probe Response frame received by the wireless LAN interface.

The interval is in 1,024 microsecond time units between target beacon transmission
times. This information is retrieved from the beacon packet sent by an access point in an infrastructure BSS network or a probe response from an access point or peer station in response to a wireless LAN client sending a Probe Request.

The IEEE 802.11 standard defines a unit of time as equal to 1,024 microseconds.  This unit was defined so that it could be easily implemented in hardware.

### -field ullTimestamp

The value of the Timestamp field from the 802.11 Beacon or Probe Response frame received by the wireless LAN interface.

### -field ullHostTimestamp

The host timestamp value that records when wireless LAN interface received the Beacon or Probe Response frame. This member is a count of 100-nanosecond intervals since January 1, 1601. 

For more information, see the <b>NdisGetCurrentSystemTime</b> function documented in the WDK.

### -field usCapabilityInformation

The value of the Capability Information field from the 802.11 Beacon or Probe Response frame received by the wireless LAN interface. This value is  a set of bit flags defining the capability. 

This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ESS"></a><a id="ess"></a><dl>
<dt><b>ESS</b></dt>
<dt>bit 0</dt>
</dl>
</td>
<td width="60%">
An extended service set. A set of one or more interconnected basic service sets (BSSs) and integrated
local area networks (LANs) that appears as a single BSS to the logical link control layer at any station
associated with one of those BSSs.

An AP set the ESS subfield to 1 and the IBSS subfield to 0 within transmitted Beacon or Probe Response
frames. A peer station within an IBSS (ad hoc network) sets the ESS subfield to 0 and the IBSS subfield to 1 in transmitted
Beacon or Probe Response frames.

</td>
</tr>
<tr>
<td width="40%"><a id="IBSS"></a><a id="ibss"></a><dl>
<dt><b>IBSS</b></dt>
<dt>bit 1</dt>
</dl>
</td>
<td width="60%">
An independent basic service set. A BSS that forms a self-contained network, and in which no
access to a distribution system (DS) is available (an ad hoc network).

An AP sets the ESS subfield to 1 and the IBSS subfield to 0 within transmitted Beacon or Probe Response
frames. A peer station within an IBSS (ad hoc network) sets the ESS subfield to 0 and the IBSS subfield to 1 in transmitted
Beacon or Probe Response frames.

</td>
</tr>
<tr>
<td width="40%"><a id="CF-Pollable"></a><a id="cf-pollable"></a><a id="CF-POLLABLE"></a><dl>
<dt><b>CF-Pollable</b></dt>
<dt>bit 2</dt>
</dl>
</td>
<td width="60%">
A value that indicates if the AP or peer station is pollable. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_Poll_Request"></a><a id="cf_poll_request"></a><a id="CF_POLL_REQUEST"></a><dl>
<dt><b>CF Poll Request</b></dt>
<dt>bit 3</dt>
</dl>
</td>
<td width="60%">
A value that indicates how the AP or peer station handles poll requests. 

</td>
</tr>
<tr>
<td width="40%"><a id="Privacy"></a><a id="privacy"></a><a id="PRIVACY"></a><dl>
<dt><b>Privacy</b></dt>
<dt>bit 4</dt>
</dl>
</td>
<td width="60%">
A value that indicates if encryption is required for all data frames. 

An AP sets the Privacy subfield to 1 within transmitted Beacon and Probe Response frames if WEP, WPA, or WPA2 encryption is required for all data type frames
exchanged within the BSS. If WEP, WPA, or WPA2 encryption is not required, the Privacy subfield is set to 0.

A peer station within and IBSS sets the Privacy subfield to 1 within transmitted Beacon and Probe Response frames if WEP, WPA, or WPA2 encryption is required for all data type frames
exchanged within the IBSS. If WEP, WPA, or WPA2 encryption is not required, the Privacy subfield is set to 0.

</td>
</tr>
</table>

### -field ulChCenterFrequency

The channel center frequency of the band on which the 802.11 Beacon or Probe Response frame was received. The value of <b>ulChCenterFrequency</b> is in units of kilohertz (kHz). 

<div class="alert"><b>Note</b>  This member is only valid for PHY types that are not frequency-hopping spread spectrum (FHSS).
</div>
<div> </div>

### -field wlanRateSet

A set of data transfer rates supported by the BSS. The data type for this member is a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_rate_set">WLAN_RATE_SET</a> structure.

### -field ulIeOffset

The offset, in bytes, of the information element (IE) data blob from the beginning of the <b>WLAN_BSS_ENTRY</b> structure.

This member points to a buffer that contains variable-length information elements (IEs) from the 802.11 Beacon or Probe Response frames. For each BSS, the IEs are from the last Beacon or Probe Response frame received from that BSS network. If an IE is available in only one frame, the wireless LAN interface driver merges the IE with the other IEs from the last received Beacon or Probe Response frame.

Information elements are defined in the IEEE 802.11 specifications to have a common general format consisting of a 1-byte Element ID field, a 1-byte Length field, and a variable-length element-specific information field. Each information element is assigned a unique
Element ID value as defined in this IEEE 802.11 standards. The Length field specifies the number of bytes in the information
field.

### -field ulIeSize

The size, in bytes, of the IE data blob in the <b>WLAN_BSS_ENTRY</b> structure. 

This is the exact length of the data in the buffer pointed to by <b>ulIeOffset</b> member and does not contain any padding for alignment. The maximum value for the size of the IE data blob is 2,324 bytes.

## -remarks

The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a> function retrieves the BSS list of the wireless network or networks on a given interface and returns this information in a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> structure that contains an array of .<b>WLAN_BSS_ENTRY</b> structures.  

 

When the wireless LAN interface is also operating as  a Wireless Hosted Network , the BSS list will contain an entry for the BSS created for the Wireless Hosted Network.



Since the information is returned by the access point for an infrastructure BSS network or by the network peer for an independent BSS network (ad hoc network), the information returned should not be trusted. The <b>ulIeOffset</b> and <b>ulIeSize</b>  members in the <b>WLAN_BSS_ENTRY</b> structure should be used to determine the maximum size of the information element data blob in the <b>WLAN_BSS_ENTRY</b> structure, not the data in the information element data blob.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a>