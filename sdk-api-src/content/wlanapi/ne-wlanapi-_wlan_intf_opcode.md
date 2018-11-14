---
UID: NE:wlanapi._WLAN_INTF_OPCODE
title: "_WLAN_INTF_OPCODE"
author: windows-sdk-content
description: Defines various opcodes used to set and query parameters on a wireless interface.
old-location: nwifi\wlan_intf_opcode.htm
tech.root: NativeWiFi
ms.assetid: 4f68e52b-7fa3-4654-b4d3-41ca627c138a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWLAN_INTF_OPCODE, PWLAN_INTF_OPCODE, PWLAN_INTF_OPCODE enumeration pointer [NativeWIFI], WLAN_INTF_OPCODE, WLAN_INTF_OPCODE enumeration [NativeWIFI], _WLAN_INTF_OPCODE, nwifi.wlan_intf_opcode, wlan_intf_opcode_autoconf_enabled, wlan_intf_opcode_autoconf_end, wlan_intf_opcode_autoconf_start, wlan_intf_opcode_background_scan_enabled, wlan_intf_opcode_bss_type, wlan_intf_opcode_certified_safe_mode, wlan_intf_opcode_channel_number, wlan_intf_opcode_current_connection, wlan_intf_opcode_current_operation_mode, wlan_intf_opcode_hosted_network_capable, wlan_intf_opcode_ihv_end, wlan_intf_opcode_ihv_start, wlan_intf_opcode_interface_state, wlan_intf_opcode_management_frame_protection_capable, wlan_intf_opcode_media_streaming_mode, wlan_intf_opcode_msm_end, wlan_intf_opcode_msm_start, wlan_intf_opcode_radio_state, wlan_intf_opcode_rssi, wlan_intf_opcode_security_end, wlan_intf_opcode_security_start, wlan_intf_opcode_statistics, wlan_intf_opcode_supported_adhoc_auth_cipher_pairs, wlan_intf_opcode_supported_country_or_region_string_list, wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs, wlan_intf_opcode_supported_safe_mode, wlanapi/PWLAN_INTF_OPCODE, wlanapi/WLAN_INTF_OPCODE, wlanapi/wlan_intf_opcode_autoconf_enabled, wlanapi/wlan_intf_opcode_autoconf_end, wlanapi/wlan_intf_opcode_autoconf_start, wlanapi/wlan_intf_opcode_background_scan_enabled, wlanapi/wlan_intf_opcode_bss_type, wlanapi/wlan_intf_opcode_certified_safe_mode, wlanapi/wlan_intf_opcode_channel_number, wlanapi/wlan_intf_opcode_current_connection, wlanapi/wlan_intf_opcode_current_operation_mode, wlanapi/wlan_intf_opcode_hosted_network_capable, wlanapi/wlan_intf_opcode_ihv_end, wlanapi/wlan_intf_opcode_ihv_start, wlanapi/wlan_intf_opcode_interface_state, wlanapi/wlan_intf_opcode_management_frame_protection_capable, wlanapi/wlan_intf_opcode_media_streaming_mode, wlanapi/wlan_intf_opcode_msm_end, wlanapi/wlan_intf_opcode_msm_start, wlanapi/wlan_intf_opcode_radio_state, wlanapi/wlan_intf_opcode_rssi, wlanapi/wlan_intf_opcode_security_end, wlanapi/wlan_intf_opcode_security_start, wlanapi/wlan_intf_opcode_statistics, wlanapi/wlan_intf_opcode_supported_adhoc_auth_cipher_pairs, wlanapi/wlan_intf_opcode_supported_country_or_region_string_list, wlanapi/wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs, wlanapi/wlan_intf_opcode_supported_safe_mode"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_INTF_OPCODE
product: Windows
targetos: Windows
req.typenames: WLAN_INTF_OPCODE, *PWLAN_INTF_OPCODE
req.redist: Wireless LAN API for Windows XP with SP2
---

# _WLAN_INTF_OPCODE enumeration


## -description


The <b>WLAN_INTF_OPCODE</b> enumerated type defines various opcodes used to set and query parameters on a wireless interface.


## -enum-fields




### -field wlan_intf_opcode_autoconf_start

Not used.


### -field wlan_intf_opcode_autoconf_enabled

The opcode used to set or query whether auto config is enabled.


### -field wlan_intf_opcode_background_scan_enabled

The opcode used to set or query whether background scan is enabled.

Background scan can only be disabled when the interface is in the connected state. Background scan is disabled if at least one client disables it.
If the interface gets disconnected, background scan will be enabled automatically.



### -field wlan_intf_opcode_media_streaming_mode

The opcode used to set or query the media streaming mode of the driver.

The media streaming mode can only be set when the interface is in the connected state. The media streaming mode is enabled if at least one client enables it.  If the interface gets disconnected, the media streaming mode is disabled automatically


### -field wlan_intf_opcode_radio_state

The opcode used to set or query the radio state.


### -field wlan_intf_opcode_bss_type

The opcode used to set or query the BSS type of the interface.


### -field wlan_intf_opcode_interface_state

The opcode used to query the state of the interface. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_current_connection

The opcode used to query information about the current connection of the interface. 

This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. If the interface is in disconnected or disconnecting state, <b>WlanQueryInterface</b> function returns <b>ERROR_INVALID_STATE</b>.


### -field wlan_intf_opcode_channel_number

The opcose used to query the current channel on which the wireless interface is operating. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs

The opcode used to query the supported auth/cipher pairs for infrastructure mode. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_supported_adhoc_auth_cipher_pairs

The opcode used to query the supported auth/cipher pairs for ad hoc mode. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_supported_country_or_region_string_list

The opcode used to query the list of supported country or region strings. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_current_operation_mode

The opcode used to set or query the current operation mode of the wireless interface. For more information about operation modes, see <a href="http://go.microsoft.com/fwlink/p/?linkid=71672">Native 802.11 Operation Modes</a>.


### -field wlan_intf_opcode_supported_safe_mode

The opcode used to query whether the miniport/NIC combination supports Federal Information Processing Standards (FIPS) mode. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. FIPS mode is also known as safe mode. This wireless safe mode is different than the operating system safe mode. 


### -field wlan_intf_opcode_certified_safe_mode

The opcode used to query whether the miniport/NIC combination is FIPS certified. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_hosted_network_capable

The opcode used to query for Hosted Network support in the device driver associated with the Wireless interface. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 

The data type returned for this opcode by a query is a Boolean. A value returned of <b>TRUE</b> indicates Hosted Network is supported. A value of <b>FALSE</b> indicates Hosted Network is not supported. 

This value is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  on Windows Server 2008 R2 with the Wireless LAN Service installed.  


### -field wlan_intf_opcode_management_frame_protection_capable

The opcode used to query whether Managememt Frame Protection (MFP) is supported in the device driver associated with the Wireless interface. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 

MFP is defined in the IEEE 802.11w-2009 amendment to 802.11 standard.

This value is supported on Windows 8 and  on Windows Server 2012.  


### -field wlan_intf_opcode_autoconf_end

Not used.


### -field wlan_intf_opcode_msm_start

Not used.


### -field wlan_intf_opcode_statistics

The opcode used to query driver statistics. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_rssi

Opcode used to query the received signal strength. This opcode can only be used in a query operation with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function. 


### -field wlan_intf_opcode_msm_end

Not used.


### -field wlan_intf_opcode_security_start

Not used.


### -field wlan_intf_opcode_security_end

Not used.


### -field wlan_intf_opcode_ihv_start

Not used.


### -field wlan_intf_opcode_ihv_end

Not used.


### -field v1_enum




## -remarks



The <b>WLAN_INTF_OPCODE</b> enumerated type defines the possible opcodes that can be passed in the <i>OpCode</i> parameter to the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> and <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> functions to query or set parameters on a wireless interface. 




## -see-also




<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>



<a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a>
 

 

