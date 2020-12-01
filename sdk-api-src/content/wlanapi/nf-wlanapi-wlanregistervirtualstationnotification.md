---
UID: NF:wlanapi.WlanRegisterVirtualStationNotification
title: WlanRegisterVirtualStationNotification function (wlanapi.h)
description: Is used to register and unregister notifications on a virtual station.
helpviewer_keywords: ["WlanRegisterVirtualStationNotification","WlanRegisterVirtualStationNotification function [NativeWIFI]","nwifi.wlanregistervirtualstationnotification","wlanapi/WlanRegisterVirtualStationNotification"]
old-location: nwifi\wlanregistervirtualstationnotification.htm
tech.root: nwifi
ms.assetid: b86ac160-ee81-43aa-86bb-cf5d3eeb2234
ms.date: 12/05/2018
ms.keywords: WlanRegisterVirtualStationNotification, WlanRegisterVirtualStationNotification function [NativeWIFI], nwifi.wlanregistervirtualstationnotification, wlanapi/WlanRegisterVirtualStationNotification
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
 - WlanRegisterVirtualStationNotification
 - wlanapi/WlanRegisterVirtualStationNotification
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
 - WlanRegisterVirtualStationNotification
---

# WlanRegisterVirtualStationNotification function


## -description

The <b>WlanRegisterVirtualStationNotification</b> function is used to register and unregister notifications on a virtual station.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param bRegister [in]

A value that specifies whether to receive notifications on a virtual station.

### -param pReserved

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>pvReserved</i> is not <b>NULL</b>.</li>
</ul>


</td>
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
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The resource is not in the correct state to perform the requested operation. This error is returned if the wireless Hosted Network is disabled by group policy on a domain.

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

The <b>WlanRegisterVirtualStationNotification</b>  function is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed. 

A client application calls the <b>WlanRegisterVirtualStationNotification</b>   function is used to register and unregister notifications on virtual station. 

Any registration to receive notifications from a virtual station caused by this function would be automatically undone if the calling application closes its calling handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter) or if the process ends.


By default, a application client will not receive notifications on a virtual station. In order to receive these notifications, a client needs to call the <b>WlanRegisterVirtualStationNotification</b> function with the <i>bRegister</i> parameter set to <b>TRUE</b> and must also call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a> function with the <i>dwNotifSource</i> parameter  set to notification sources to be registered. The registration to receive notifications from a virtual station is in effect until the application closes the client handle (by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a> with the <i>hClientHandle</i> parameter), the process ends, or the <b>WlanRegisterVirtualStationNotification</b> function is called with the <i>bRegister</i> parameter set to <b>FALSE</b>.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well. This feature is also available on Windows Server 2008 R2 with the Wireless LAN Service installed.

## -see-also

<a href="/windows/desktop/NativeWiFi/about-the-wireless-hosted-network">About the Wireless Hosted Network</a>



<a href="/windows/desktop/NativeWiFi/using-hosted-network-and-internet-connection-sharing">Using Wireless Hosted Network and Internet Connection Sharing</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>