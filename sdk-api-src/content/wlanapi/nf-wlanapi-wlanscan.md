---
UID: NF:wlanapi.WlanScan
title: WlanScan function (wlanapi.h)
description: Requests a scan for available networks on the indicated interface.
helpviewer_keywords: ["WlanScan","WlanScan function [NativeWIFI]","nwifi.wlanscan","wlanapi/WlanScan"]
old-location: nwifi\wlanscan.htm
tech.root: nwifi
ms.assetid: cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1
ms.date: 12/05/2018
ms.keywords: WlanScan, WlanScan function [NativeWIFI], nwifi.wlanscan, wlanapi/WlanScan
req.header: wlanapi.h
req.include-header: Wlanapi.h
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanScan
 - wlanapi/WlanScan
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
 - WlanScan
---

# WlanScan function

## -description

> [!NOTE]
> **Some information relates to pre-released product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.**

> [!IMPORTANT]
> This API will be affected by upcoming changes to operating system behavior, planned for fall 2024. For more info, see [Changes to API behavior for Wi-Fi access and location](/windows/win32/nativewifi/wi-fi-access-location-changes).

The <b>WlanScan</b> function requests a scan for available networks on the indicated interface.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface to be queried.

 The GUID of each wireless LAN interface enabled on a local computer can be determined using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

### -param pDot11Ssid [in, optional]

A pointer to a <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure that specifies the SSID of the network to be scanned. This parameter may be <b>NULL</b>. 
<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This parameter must be <b>NULL</b>.

### -param pIeData [in, optional]

A pointer to an information element to include in probe requests. This parameter points to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data">WLAN_RAW_DATA</a> structure that may include client provisioning availability information and 802.1X authentication requirements.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This parameter must be <b>NULL</b>.

### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>.

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
<i>hClientHandle</i> is <b>NULL</b> or invalid,  <i>pInterfaceGuid</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

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
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory for the query results.

</td>
</tr>
</table>

## -remarks

The <b>WlanScan</b> function requests that the native 802.11 Wireless LAN driver scan for available wireless networks. The driver may or may not send probe requests (an active scan) depending on its implementation and the values passed in the <i>pDot11Ssid</i> and <i>pIeData</i> parameters. 

If the <i>pIeData</i> parameter is not <b>NULL</b>, the driver will send probe requests during the scan. The probe requests include the information element (IE) pointed to by the <i>pIeData</i> parameter. For instance, the Wi-Fi Protected Setup (WPS) IE can be included in the probe requests to discover WPS-capable access points. The buffer pointed to by the <i>pIeData</i> parameter must contain the complete IE starting from the Element ID.

The <i>pIeData</i> parameter passed to the <b>WlanScan</b> function can contain a pointer to an optional <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data">WLAN_RAW_DATA</a> structure that contains a proximity service discovery (PSD) IE data entry.   

When used to store a PSD IE, the <b>DOT11_PSD_IE_MAX_DATA_SIZE</b> constant defined in the <i>Wlanapi.h</i> header file is the maximum value of the <b>dwDataSize</b> member.<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>DOT11_PSD_IE_MAX_DATA_SIZE</b></td>
<td>240</td>
<td>The maximum data size, in bytes, of a PSD IE data entry.</td>
</tr>
</table>
 



For more information about PSD IEs, including a discussion of the format of a PSD IE, see the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetpsdiedatalist">WlanSetPsdIEDataList</a> function.

When the <b>WlanScan</b> function is called, the native 802.11 Wireless LAN driver may flush the current list of available wireless networks before the scan is initiated. Applications should not assume that calling the <b>WlanScan</b> function will add to the existing list of available wireless networks returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a> functions from previous scans.

The <b>WlanScan</b> function returns immediately.  To be notified when the network scan is complete, a client on Windows Vista and later  must register for notifications by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>. The <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function must have the WLAN_NOTIFICATION_SOURCE_ACM bit set to register for notifications generated by the auto configuration module. Wireless network drivers that meet Windows logo requirements are required to complete a <b>WlanScan</b> function request in 4 seconds. 

The Wireless LAN Service does not send notifications when available wireless networks change. The Wireless LAN Service does not track changes to the list of available networks across multiple scans. The current default behavior is that the Wireless LAN Service only asks the wireless interface driver to scan for wireless networks every 60 seconds, and in some cases (when already connected to wireless network) the Wireless LAN Service does not ask for scans at all.
 The <b>WlanScan</b> function can be used by an application to track wireless network changes.  The application should first register for WLAN_NOTIFICATION_SOURCE_ACM notifications. The <b>WlanScan</b> function can then be called to initiate a scan. The application should then wait to receive the wlan_notification_acm_scan_complete notification or timeout after 4 seconds. Then the application can call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a> function to retrieve a list of available wireless networks. This process can be repeated periodically with the application keeping tracking of changes to available wireless networks.

The <b>WlanScan</b> function returns immediately and does not provide a notification when the scan is complete on Windows XP with SP3 or the Wireless LAN API for Windows XP with SP2.  

Since it becomes more difficult for a wireless interface to send and receive data packets while a scan is occurring, the <b>WlanScan</b> function may increase latency until the network scan is complete.

## -see-also

<a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data">WLAN_RAW_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist">WlanGetAvailableNetworkList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetpsdiedatalist">WlanSetPsdIEDataList</a>
