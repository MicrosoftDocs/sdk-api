---
UID: NF:wlanapi.WlanScan
title: WlanScan function
author: windows-driver-content
description: Requests a scan for available networks on the indicated interface.
old-location: nwifi\wlanscan.htm
old-project: NativeWiFi
ms.assetid: cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: WlanScan, WlanScan function [NativeWIFI], nwifi.wlanscan, wlanapi/WlanScan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wlanapi.dll
api_name:
-	WlanScan
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanScan function


## -description


The <b>WlanScan</b> function requests a scan for available networks on the indicated interface.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface to be queried.

 The GUID of each wireless LAN interface enabled on a local computer can be determined using the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function.


### -param pDot11Ssid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff548773">DOT11_SSID</a> structure that specifies the SSID of the network to be scanned. This parameter is optional. When set to <b>NULL</b>, the returned list contains all available networks. 
<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This parameter must be <b>NULL</b>.




### -param pIeData [in, optional]

A pointer to an information element to include in probe requests. This parameter points to a <a href="https://msdn.microsoft.com/5f5ddecb-f841-436c-bf31-c70c95a5d39c">WLAN_RAW_DATA</a> structure that may include client provisioning availability information and 802.1X authentication requirements.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>This parameter must be <b>NULL</b>.




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

The <i>pIeData</i> parameter passed to the <b>WlanScan</b> function can contain a pointer to an optional <a href="https://msdn.microsoft.com/5f5ddecb-f841-436c-bf31-c70c95a5d39c">WLAN_RAW_DATA</a> structure that contains a proximity service discovery (PSD) IE data entry.   

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
 



For more information about PSD IEs, including a discussion of the format of a PSD IE, see the <a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a> function.

When the <b>WlanScan</b> function is called, the native 802.11 Wireless LAN driver may flush the current list of available wireless networks before the scan is initiated. Applications should not assume that calling the <b>WlanScan</b> function will add to the existing list of available wireless networks returned by the <a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a> or <a href="https://msdn.microsoft.com/27353a1b-2a3c-4c3b-b512-917d010ee8dd">WlanGetAvailableNetworkList</a> functions from previous scans.

The <b>WlanScan</b> function returns immediately.  To be notified when the network scan is complete, a client on Windows Vista and later  must register for notifications by calling <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>. The <i>dwNotifSource</i> parameter passed to the <b>WlanRegisterNotification</b> function must have the WLAN_NOTIFICATION_SOURCE_ACM bit set to register for notifications generated by the auto configuration module. Wireless network drivers that meet Windows logo requirements are required to complete a <b>WlanScan</b> function request in 4 seconds. 

The Wireless LAN Service does not send notifications when available wireless networks change. The Wireless LAN Service does not track changes to the list of available networks across multiple scans. The current default behavior is that the Wireless LAN Service only asks the wireless interface driver to scan for wireless networks every 60 seconds, and in some cases (when already connected to wireless network) the Wireless LAN Service does not ask for scans at all.
 The <b>WlanScan</b> function can be used by an application to track wireless network changes.  The application should first register for WLAN_NOTIFICATION_SOURCE_ACM notifications. The <b>WlanScan</b> function can then be called to initiate a scan. The application should then wait to receive the wlan_notification_acm_scan_complete notification or timeout after 4 seconds. Then the application can call the <a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a> or <a href="https://msdn.microsoft.com/27353a1b-2a3c-4c3b-b512-917d010ee8dd">WlanGetAvailableNetworkList</a> function to retrieve a list of available wireless networks. This process can be repeated periodically with the application keeping tracking of changes to available wireless networks.

The <b>WlanScan</b> function returns immediately and does not provide a notification when the scan is complete on Windows XP with SP3 or the Wireless LAN API for Windows XP with SP2.  

Since it becomes more difficult for a wireless interface to send and receive data packets while a scan is occurring, the <b>WlanScan</b> function may increase latency until the network scan is complete.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548773">DOT11_SSID</a>



<a href="https://msdn.microsoft.com/5f5ddecb-f841-436c-bf31-c70c95a5d39c">WLAN_RAW_DATA</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/27353a1b-2a3c-4c3b-b512-917d010ee8dd">WlanGetAvailableNetworkList</a>



<a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a>



<a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a>



<a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a>
 

 

