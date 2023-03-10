---
UID: NF:wlanapi.WlanSetPsdIEDataList
title: WlanSetPsdIEDataList function (wlanapi.h)
description: Sets the proximity service discovery (PSD) information element (IE) data list.
helpviewer_keywords: ["WlanSetPsdIEDataList","WlanSetPsdIEDataList function [NativeWIFI]","nwifi.wlansetpsdiedatalist","wlanapi/WlanSetPsdIEDataList"]
old-location: nwifi\wlansetpsdiedatalist.htm
tech.root: nwifi
ms.assetid: eea402d3-9a5f-4446-bf6c-9ab8430f9c60
ms.date: 12/05/2018
ms.keywords: WlanSetPsdIEDataList, WlanSetPsdIEDataList function [NativeWIFI], nwifi.wlansetpsdiedatalist, wlanapi/WlanSetPsdIEDataList
req.header: wlanapi.h
req.include-header: Wlanapi.h
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlanSetPsdIEDataList
 - wlanapi/WlanSetPsdIEDataList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanSetPsdIEDataList
---

# WlanSetPsdIEDataList function


## -description

The <b>WlanSetPsdIeDataList</b> function sets the proximity service discovery (PSD) information element (IE) data list.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param strFormat [in]

The format of a PSD IE in the PSD IE data list passed in the <i>pPsdIEDataList</i> parameter. This is a NULL-terminated URI string that specifies the namespace of the protocol used for discovery.

### -param pPsdIEDataList [in]

A pointer to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data_list">WLAN_RAW_DATA_LIST</a> structure that contains the PSD IE data list to be set.

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A  parameter is incorrect. This error is returned if the <i>hClientHandle</i> is <b>NULL</b> or not valid or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value is returned if the function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>

## -remarks

The Proximity Service Discovery Protocol is a Microsoft proprietary protocol that allows a client to discover services in its physical proximity, which is defined by the radio range. The purpose of the Proximity Service Discovery Protocol is to convey service discovery information, such as service advertisements, as part of Beacon frames. Access points (APs) and stations (STAs) that operate in ad hoc mode periodically broadcast beacon frames. The beacon frame can contain single or multiple proprietary information elements that carry discovery information pertaining to the services that the device offers.

A PSD IE is used to transmit compressed information provided by higher-level discovery protocols for the purpose of passive discovery. One such higher-level protocol used for discovery is the WS-Discovery protocol. Any protocol can be used for discovery. 

Windows Vista and Windows Server 2008 with the Wireless LAN Service installed support passive discovery for ad hoc clients, ad hoc services, and infrastructure clients. This means an ad hoc service can advertise an available resource or service by transmitting a PSD IE in one or more beacons. There is no guarantee that this beacon is received by an ad hoc or infrastructure client. 

Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed  support passive discovery for ad hoc clients, ad hoc services, and infrastructure clients in the same way as in Windows Vista. In addition, the PSD IE is also supported for the wireless Hosted Network, a software-based wireless access point (AP). Applications on the local computer where the wireless Hosted Network is to be run may use the <b>WlanSetPsdIeDataList</b> function to set the PSD IE before starting the wireless Hosted Network. Once set, the PSD IE will be included in the beacon and probe response after the wireless Hosted Network is started.

Each application sending or receiving beacons maintains its own PSD IE data list. The <i>pPsdIEDataList</i> parameter points to a list of PSD IEs generated by the application.  Each PSD IE has the following format.<table>
<tr>
<th>Field</th>
<th>Description and Value</th>
</tr>
<tr>
<td>Element ID (1 byte)</td>
<td>221</td>
</tr>
<tr>
<td>Length (1 byte)</td>
<td>The length, in bytes, of Data field plus 8. </td>
</tr>
<tr>
<td>OUI (3 bytes)</td>
<td>The Organizational Unique Identifier (OUI) must contain a value of 00-50-F2. This public OUI is registered to Microsoft.</td>
</tr>
<tr>
<td>OUI Type (1 byte)</td>
<td>For the Proximity Service Discovery Protocol, the OUI Type must contain a value of 6.</td>
</tr>
<tr>
<td>Format identifier hash(4 bytes)</td>
<td>Bits 31-0 of the HMAC computed from the <i>strFormat</i> parameter. </td>
</tr>
<tr>
<td>Data (variable)</td>
<td>Contains user-defined data for discovery.  This field must not exceed 240 bytes in length.</td>
</tr>
</table>
 </p>Element ID 221 specifies the Vendor-Specific information element defined in the IEEE 802.11 standards. The Organizational Unique Identifier (OUI) contains a 3-byte, IEEE-assigned OUI of the vendor that defined the content of the information element in the same order that the OUI would be transmitted in an IEEE 802.11 address field. The Element ID, Length, OUI, and OUI Type fields are controlled by the automatic configuration service, while the application controls the rest of the fields. 

The Format identifier hash field describes the format of the information carried in the PSD IE. To ensure uniqueness while circumventing the need for central administration of format identifiers, a string in the form of a Uniform Resource Identifier (URI), as specified in <a href="http://tools.ietf.org/html/rfc3986">RFC 3986</a>, is used to distinguish the format. However, because the transmission must be efficient and space in the information element is limited, the string is not actually transmitted, but, instead, its hash is transmitted. On the client, which is the receiving side of the beacon, the hash is matched against a known set of format identifiers.

The Format identifier hash field is represented by bits 0…31 of a hash-based message authentication code (HMAC) over the format identifier string specified in the <i>strFormat</i> parameter. The HMAC is used to specify the format of the Data field of the PSD  IE. The formula used to calculate the HMAC is described in <a href="https://www.ietf.org/rfc/rfc2104.txt">RFC 2104</a>. Sample code for the calculation of the HMAC is as specified in <a href="http://tools.ietf.org/html/rfc4634">RFC 4634</a>. When calculating the HMAC, use SHA-256 for the hash function. The key used is the "null" key (<b>NULL</b> pointer to the authentication key, and zero length authentication key per the source code in <a href="http://tools.ietf.org/html/rfc4634">RFC 4634</a>). Use the value of <i>strFormat</i> parameter (including any spaces but excluding the NULL-termination character) as the input text encoded as Unicode UTF-16 in little-endian format.

For example, if the <i>strFormat</i> parameter is <code>http://schemas.xmlsoaps.org/ws/2004/10/discovery</code>, then the first four octets of the corresponding HMAC is <code>0xF8 0xCB 0x35 0x15</code>. 

If the <i>strFormat</i> parameter is <code>http://schemas.microsoft.com/networking/discoveryformat/v2</code>, then the four octets of the corresponding HMAC are <code>0xCF 0xF1 0x64 0x17</code>. 

When sending the first 4 octets of an HMAC over the network, send the first (left-most) octet first.

Note that there may be collisions in the truncated HMACs, which means that it may be impossible to uniquely determine the discovery protocol corresponding to the payload of a PSD IE from the given bits of an HMAC. An application receiving a PSD IE must take a best guess at the discovery protocol used from a given HMAC, then re-run the higher-level discovery protocol once a connection has been established.

At most, five PSD IEs can be passed in a list. Also, the total length, in bytes, of the PSD IE list may be restricted by hardware limitations on the length of a beacon.

An application can call  <b>WlanSetPsdIeDataList</b> many times. When <b>WlanSetPsdIeDataList</b>  is called twice with the same <i>strFormat</i>, the contents of the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data_list">WLAN_RAW_DATA_LIST</a> populated by the first function call are overwritten by the second call's <b>WLAN_RAW_DATA_LIST</b> payload. When <b>WlanSetPsdIeDataList</b>  is called with the <i>pPsdIEDataList</i> parameter set to <b>NULL</b>, the PSD IE list associated with <i>strFormat</i> is cleared. When <b>WlanSetPsdIeDataList</b>  is called with both the <i>pPsdIEDataList</i>  and <i>strFormat</i> parameters set to <b>NULL</b>, all PSD IE lists set by the application are cleared. 

The wireless service processes PSD IE data lists set by different applications and generates  raw IE data blobs. When a machine creates or joins an ad-hoc network on any wireless adapter, it sends beacons that include a PSD IE data blob associated with the network to other machines. 

Stations can call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanextractpsdiedatalist">WlanExtractPsdIEDataList</a> function to get the PSD IE data list after receiving a beacon from a machine.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data_list">WLAN_RAW_DATA_LIST</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanextractpsdiedatalist">WlanExtractPsdIEDataList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan">WlanScan</a>