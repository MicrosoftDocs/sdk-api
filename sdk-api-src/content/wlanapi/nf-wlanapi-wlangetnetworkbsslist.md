---
UID: NF:wlanapi.WlanGetNetworkBssList
title: WlanGetNetworkBssList function (wlanapi.h)
description: Retrieves a list of the basic service set (BSS) entries of the wireless network or networks on a given wireless LAN interface.
helpviewer_keywords: ["WlanGetNetworkBssList","WlanGetNetworkBssList function [NativeWIFI]","dot11_BSS_type_any","dot11_BSS_type_independent","dot11_BSS_type_infrastructure","nwifi.wlangetnetworkbsslist","wlanapi/WlanGetNetworkBssList"]
old-location: nwifi\wlangetnetworkbsslist.htm
tech.root: nwifi
ms.assetid: 62f51b6e-3db1-48cd-8853-0dbe522c5e82
ms.date: 12/05/2018
ms.keywords: WlanGetNetworkBssList, WlanGetNetworkBssList function [NativeWIFI], dot11_BSS_type_any, dot11_BSS_type_independent, dot11_BSS_type_infrastructure, nwifi.wlangetnetworkbsslist, wlanapi/WlanGetNetworkBssList
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
 - WlanGetNetworkBssList
 - wlanapi/WlanGetNetworkBssList
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
 - WlanGetNetworkBssList
---

# WlanGetNetworkBssList function

## -description

> [!NOTE]
> **Some information relates to pre-released product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.**

> [!IMPORTANT]
> This API will be affected by upcoming changes to operating system behavior, planned for fall 2024. For more info, see [Changes to API behavior for Wi-Fi access and location](/windows/win32/nativewifi/wi-fi-access-location-changes).

The <b>WlanGetNetworkBssList</b> function retrieves a list of the basic service set (BSS) entries of the wireless network or networks on a given wireless LAN interface.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

A pointer to the GUID of the wireless LAN interface to be queried.

 The GUID of each wireless LAN interface enabled on a local computer can be determined using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

### -param pDot11Ssid [optional]

A pointer to a <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that specifies the SSID of the network from which the BSS list is requested.  This parameter is optional. When set to <b>NULL</b>, the returned list contains all of available BSS entries on a wireless LAN interface.

If a pointer to a <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure is specified, the SSID length specified in the <b>uSSIDLength</b> member of <b>DOT11_SSID</b> structure must be less than or equal to <b>DOT11_SSID_MAX_LENGTH</b> defined in the <i>Wlantypes.h</i> header file. In addition, the <i>dot11BssType</i> parameter must be set to either <b>dot11_BSS_type_infrastructure</b> or <b>dot11_BSS_type_independent</b> and the <i>bSecurityEnabled</i> parameter must be specified.

### -param dot11BssType [in]

The BSS type of the network. This parameter is ignored if the SSID of the network for the BSS list is unspecified (the <i>pDot11Ssid</i> parameter is <b>NULL</b>). 

This parameter can be one of the following values defined in the <a href="/windows/desktop/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a> enumeration defined in the <i>Wlantypes.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dot11_BSS_type_infrastructure"></a><a id="dot11_bss_type_infrastructure"></a><a id="DOT11_BSS_TYPE_INFRASTRUCTURE"></a><dl>
<dt><b>dot11_BSS_type_infrastructure</b></dt>
</dl>
</td>
<td width="60%">
An infrastructure BSS network.

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_BSS_type_independent_"></a><a id="dot11_bss_type_independent_"></a><a id="DOT11_BSS_TYPE_INDEPENDENT_"></a><dl>
<dt><b>dot11_BSS_type_independent </b></dt>
</dl>
</td>
<td width="60%">
An independent BSS (IBSS) network (an ad hoc network).

</td>
</tr>
<tr>
<td width="40%"><a id="dot11_BSS_type_any"></a><a id="dot11_bss_type_any"></a><a id="DOT11_BSS_TYPE_ANY"></a><dl>
<dt><b>dot11_BSS_type_any</b></dt>
</dl>
</td>
<td width="60%">
Any BSS network. 

</td>
</tr>
</table>

### -param bSecurityEnabled [in]

A value that indicates whether security is enabled on the network.  This parameter is only valid when the SSID of the network for the BSS list is specified (the <i>pDot11Ssid</i> parameter is not <b>NULL</b>).

### -param pReserved

Reserved for future use.  This parameter must be set to <b>NULL</b>.

### -param ppWlanBssList [out]

A pointer to storage for a pointer to receive the returned list of BSS entries in a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> structure. 

The buffer for the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> returned is allocated by the <b>WlanGetNetworkBssList</b> function if the call succeeds.

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
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>hClientHandle</i>,  <i>pInterfaceGuid</i>, or <i>ppWlanBssList</i> parameter is <b>NULL</b>. This error is returned if the <i>pReserved</i> is not <b>NULL</b>. This error is also returned if the <i>hClientHandle</i>, the SSID specified in the <i>pDot11Ssid</i> parameter, or the BSS type specified in the <i>dot11BssType</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NDIS_DOT11_POWER_STATE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The radio associated with the interface is turned off. The BSS list is not available when the radio is off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to process this request and allocate memory for the query results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element was not found. This error is returned if the GUID of the interface to be queried that was specified in the <i>pInterfaceGuid</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if this function was called from a  Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client. This error is also returned if the WLAN AutoConfig service is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The WLAN AutoConfig service has not been started.

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

The <b>WlanGetNetworkBssList</b> function retrieves the basic service set list for each wireless network or networks accessible on a given interface. The list of information returned for each wireless network also contains a list of information elements returned by each access point for an infrastructure BSS network or a network peer for an independent BSS network (ad hoc network). The information is returned as a pointer to an <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> structure in the <i>ppWlanBssList</i> parameter.  The <b>WLAN_BSS_LIST</b> structure contains an item count followed by an array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a> structure entries.  

Since the information returned by the <b>WlanGetNetworkBssList</b> function is sent by an access point for an infrastructure BSS network or by a network peer for an independent BSS network (ad hoc network), the information returned should not be trusted. The <b>ulIeOffset</b> and <b>ulIeSize</b>  members in the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a> structure should be used to determine the size of the information element data blob in the <b>WLAN_BSS_ENTRY</b> structure, not the data in the information element data blob itself. The <b>WlanGetNetworkBssList</b> function does not validate that any information returned in the information element data blob pointed to by the <b>ulIeOffset</b> member is a valid information element as defined by the IEEE 802.11 standards for wireless LANs.

If the <i>pDot11Ssid</i> parameter is specified (not <b>NULL</b>), then the <i>dot11BssType</i> parameter specified must be set to either <b>dot11_BSS_type_infrastructure</b> for an infrastructure BSS network or <b>dot11_BSS_type_independent</b> for an independent BSS network (ad hoc network). If the <i>dot11BssType</i> parameter is set to <b>dot11_BSS_type_any</b>, then the <b>WlanGetNetworkBssList</b>  function returns ERROR_SUCCESS  but no BSS entries will be returned.

To return a list of all the infrastructure BSS networks and independent BSS  networks (ad hoc networks) on a wireless LAN interface, set the <i>pDot11Ssid</i> parameter to <b>NULL</b>. When the wireless LAN interface is also operating as  a Wireless Hosted Network , the BSS list will contain an entry for the BSS created for the Wireless Hosted Network.



The <b>WlanGetNetworkBssList</b>  function returns ERROR_SUCCESS when an empty BSS list is returned by the WLAN AutoConfig Service. An application that calls  the <b>WlanGetNetworkBssList</b>  function must check that the <b>dwNumberOfItems</b> member of the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a> pointed to by the <i>ppWlanBssList</i> parameter is not zero before accessing the <b>wlanBssEntries[0]</b> member in <b>WLAN_BSS_LIST</b> structure. 

The <b>WlanGetNetworkBssList</b> function allocates memory for the basic service set list that is returned in a buffer pointed to by the <i>ppWlanBssList</i> parameter when the function succeeds. The memory used for the buffer pointed to by <i>ppWlanBssList</i> parameter should be released by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function after the buffer is no longer needed.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan">WlanScan</a>