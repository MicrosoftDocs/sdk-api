---
UID: NE:wlanapi._WLAN_HOSTED_NETWORK_REASON
title: "_WLAN_HOSTED_NETWORK_REASON"
author: windows-sdk-content
description: Specifies the possible values for the result of a wireless Hosted Network function call.
old-location: nwifi\wlan_hosted_network_reason.htm
old-project: NativeWiFi
ms.assetid: affca9ab-fcd4-474d-993c-f6bb6b1f967c
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_REASON, PWLAN_HOSTED_NETWORK_REASON, PWLAN_HOSTED_NETWORK_REASON enumeration pointer [NativeWIFI], WLAN_HOSTED_NETWORK_REASON, WLAN_HOSTED_NETWORK_REASON enumeration [NativeWIFI], _WLAN_HOSTED_NETWORK_REASON, nwifi.wlan_hosted_network_reason, wlan_hosted_network_reason_ap_start_failed, wlan_hosted_network_reason_bad_parameters, wlan_hosted_network_reason_client_abort, wlan_hosted_network_reason_crypt_error, wlan_hosted_network_reason_device_change, wlan_hosted_network_reason_elevation_required, wlan_hosted_network_reason_gp_denied, wlan_hosted_network_reason_impersonation, wlan_hosted_network_reason_incompatible_connection_started, wlan_hosted_network_reason_incompatible_connection_stopped, wlan_hosted_network_reason_insufficient_resources, wlan_hosted_network_reason_interface_available, wlan_hosted_network_reason_interface_unavailable, wlan_hosted_network_reason_miniport_started, wlan_hosted_network_reason_miniport_stopped, wlan_hosted_network_reason_peer_arrived, wlan_hosted_network_reason_peer_departed, wlan_hosted_network_reason_peer_timeout, wlan_hosted_network_reason_persistence_failed, wlan_hosted_network_reason_properties_change, wlan_hosted_network_reason_read_only, wlan_hosted_network_reason_service_available_on_virtual_station, wlan_hosted_network_reason_service_shutting_down, wlan_hosted_network_reason_service_unavailable, wlan_hosted_network_reason_stop_before_start, wlan_hosted_network_reason_success, wlan_hosted_network_reason_unspecified, wlan_hosted_network_reason_user_action, wlan_hosted_network_reason_virtual_station_blocking_use, wlanapi/PWLAN_HOSTED_NETWORK_REASON, wlanapi/WLAN_HOSTED_NETWORK_REASON, wlanapi/wlan_hosted_network_reason_ap_start_failed, wlanapi/wlan_hosted_network_reason_bad_parameters, wlanapi/wlan_hosted_network_reason_client_abort, wlanapi/wlan_hosted_network_reason_crypt_error, wlanapi/wlan_hosted_network_reason_device_change, wlanapi/wlan_hosted_network_reason_elevation_required, wlanapi/wlan_hosted_network_reason_gp_denied, wlanapi/wlan_hosted_network_reason_impersonation, wlanapi/wlan_hosted_network_reason_incompatible_connection_started, wlanapi/wlan_hosted_network_reason_incompatible_connection_stopped, wlanapi/wlan_hosted_network_reason_insufficient_resources, wlanapi/wlan_hosted_network_reason_interface_available, wlanapi/wlan_hosted_network_reason_interface_unavailable, wlanapi/wlan_hosted_network_reason_miniport_started, wlanapi/wlan_hosted_network_reason_miniport_stopped, wlanapi/wlan_hosted_network_reason_peer_arrived, wlanapi/wlan_hosted_network_reason_peer_departed, wlanapi/wlan_hosted_network_reason_peer_timeout, wlanapi/wlan_hosted_network_reason_persistence_failed, wlanapi/wlan_hosted_network_reason_properties_change, wlanapi/wlan_hosted_network_reason_read_only, wlanapi/wlan_hosted_network_reason_service_available_on_virtual_station, wlanapi/wlan_hosted_network_reason_service_shutting_down, wlanapi/wlan_hosted_network_reason_service_unavailable, wlanapi/wlan_hosted_network_reason_stop_before_start, wlanapi/wlan_hosted_network_reason_success, wlanapi/wlan_hosted_network_reason_unspecified, wlanapi/wlan_hosted_network_reason_user_action, wlanapi/wlan_hosted_network_reason_virtual_station_blocking_use"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WLAN_HOSTED_NETWORK_REASON, *PWLAN_HOSTED_NETWORK_REASON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_REASON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_HOSTED_NETWORK_REASON enumeration


## -description


The <b>WLAN_HOSTED_NETWORK_REASON</b> enumerated type specifies the possible values for the result of a wireless Hosted Network function call.


## -enum-fields




### -field wlan_hosted_network_reason_success

The operation was successful.


### -field wlan_hosted_network_reason_unspecified

Unknown error.


### -field wlan_hosted_network_reason_bad_parameters

Bad parameters.

For example, this reason code is returned if an application failed to reference the client context from the correct handle (the handle returned by the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function).


### -field wlan_hosted_network_reason_service_shutting_down

Service is shutting down.


### -field wlan_hosted_network_reason_insufficient_resources

Service is out of resources.


### -field wlan_hosted_network_reason_elevation_required

This operation requires elevation.


### -field wlan_hosted_network_reason_read_only

An attempt was made to write read-only data.


### -field wlan_hosted_network_reason_persistence_failed

Data persistence failed.


### -field wlan_hosted_network_reason_crypt_error

A cryptographic error occurred.


### -field wlan_hosted_network_reason_impersonation

User impersonation failed.


### -field wlan_hosted_network_reason_stop_before_start

An incorrect function call sequence was made.


### -field wlan_hosted_network_reason_interface_available

A wireless interface has become available.


### -field wlan_hosted_network_reason_interface_unavailable

A wireless interface has become unavailable.

This reason code is returned by the wireless Hosted Network functions any time the network state of the wireless Hosted Network is <b>wlan_hosted_network_unavailable</b>. For example if the wireless Hosted Network is disabled by group policy on a domain, then the  network state of the wireless Hosted Network is <b>wlan_hosted_network_unavailable</b>. In this case, any calls to the <a href="https://msdn.microsoft.com/923ffc09-f378-442c-a891-34b0c0d04c41">WlanHostedNetworkStartUsing</a> or <a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a> function  would return this reason code.


### -field wlan_hosted_network_reason_miniport_stopped

The wireless miniport driver stopped the Hosted Network.


### -field wlan_hosted_network_reason_miniport_started

The wireless miniport driver status changed.


### -field wlan_hosted_network_reason_incompatible_connection_started

An incompatible connection started.

An incompatible connection refers to one of the following cases:<ul>
<li>An ad hoc wireless connection is started on the primary station adapter.</li>
<li>Network monitoring is started on the primary station adapter by an application (Network Monitor, for example) that calls the <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> function with the <i>OpCode</i> parameter set to  <b>wlan_intf_opcode_current_operation_mode</b> and the <i>pData</i> parameter points to a ULONG that contains <b>DOT11_OPERATION_MODE_NETWORK_MONITOR</b>. </li>
<li>A wireless connection is started in FIPS safe mode on the primary station adapter. FIPS safe mode is specified in the profile of the wireless connection. For more information, see the <a href="https://msdn.microsoft.com/4c62c96c-82e7-4174-b833-95ee10b29344">FIPSMode Element</a> .
</li>
</ul>


Windows will stop the wireless Hosted Network on  the software-based wireless access point (AP) adapter when an incompatible connection starts on the primary station adapter. The network state of the wireless Hosted Network state would become <b>wlan_hosted_network_unavailable</b>. 


### -field wlan_hosted_network_reason_incompatible_connection_stopped

An incompatible connection stopped.

An incompatible connection previously started on the primary station adapter (wlan_hosted_network_reason_incompatible_connection_started), but the incompatible connection has stopped. If the wireless Hosted Network was previously stopped as a result of an incompatible connection being started, Windows will not automatically restart the wireless Hosted Network. Applications can restart the wireless Hosted Network on the AP adapter by calling the <a href="https://msdn.microsoft.com/923ffc09-f378-442c-a891-34b0c0d04c41">WlanHostedNetworkStartUsing</a> or <a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a> function.


### -field wlan_hosted_network_reason_user_action

A state change occurred that was caused by explicit user action.


### -field wlan_hosted_network_reason_client_abort

A state change occurred that was caused by client abort.


### -field wlan_hosted_network_reason_ap_start_failed

The driver for the wireless Hosted Network failed to start.


### -field wlan_hosted_network_reason_peer_arrived

A peer connected to the wireless Hosted Network.


### -field wlan_hosted_network_reason_peer_departed

A peer disconnected from the wireless Hosted Network.


### -field wlan_hosted_network_reason_peer_timeout

A peer timed out.


### -field wlan_hosted_network_reason_gp_denied

The operation was denied by group policy.


### -field wlan_hosted_network_reason_service_unavailable

The Wireless LAN service is not running.


### -field wlan_hosted_network_reason_device_change

The wireless adapter used by the wireless Hosted Network changed.


### -field wlan_hosted_network_reason_properties_change

The properties of the wireless Hosted Network changed.


### -field wlan_hosted_network_reason_virtual_station_blocking_use

A virtual station is active and blocking operation.


### -field wlan_hosted_network_reason_service_available_on_virtual_station

An identical service is available on a virtual station.


### -field v1_enum




## -remarks



The <b>WLAN_HOSTED_NETWORK_REASON</b> enumerated type is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  

The <b>WLAN_HOSTED_NETWORK_REASON</b> enumerates the possible reasons that a wireless Hosted Network function call failed or the reasons why a particular wireless Hosted Network notification was generated.

On Windows 7 and later, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine. This virtual device normally shows up in the “Network Connections Folder” as ‘Wireless  Network Connection 2’ with a Device Name of ‘Microsoft Virtual WiFi Miniport adapter’ if the computer has a single wireless network adapter. This virtual device is used exclusively for performing software access point (SoftAP) connections and is not present in the list returned by the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. The lifetime of this virtual device is tied to the physical wireless adapter. If the physical wireless adapter is disabled, this virtual device will be removed as well.




## -see-also




<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/d3e3b44f-ff52-4062-b54d-a0e3f2cf7785">WlanHostedNetworkForceStart</a>



<a href="https://msdn.microsoft.com/abcfc33d-0310-46d2-a543-5c9529c2b851">WlanHostedNetworkForceStop</a>



<a href="https://msdn.microsoft.com/aed4db5d-9740-43ee-bf09-7a4a5abae953">WlanHostedNetworkInitSettings</a>



<a href="https://msdn.microsoft.com/5989977a-7a2f-43b8-a958-058db01fd24f">WlanHostedNetworkQuerySecondaryKey</a>



<a href="https://msdn.microsoft.com/9589e3a6-6e7a-4186-bfd0-a942a39ecafb">WlanHostedNetworkRefreshSecuritySettings</a>



<a href="https://msdn.microsoft.com/88139383-f5d5-4e42-b41e-ea754a89356d">WlanHostedNetworkSetProperty</a>



<a href="https://msdn.microsoft.com/385148fd-b5cd-4221-be25-077f484e93e9">WlanHostedNetworkSetSecondaryKey</a>



<a href="https://msdn.microsoft.com/923ffc09-f378-442c-a891-34b0c0d04c41">WlanHostedNetworkStartUsing</a>



<a href="https://msdn.microsoft.com/36b5ed93-33c4-4ade-a6d9-0d240854a5ef">WlanHostedNetworkStopUsing</a>
 

 

