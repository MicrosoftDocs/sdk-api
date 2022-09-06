---
UID: NE:wlanapi._WLAN_INTF_OPCODE~r1
title: WLAN_INTF_OPCODE
ms.date: 01/30/2019
ms.keywords: _WLAN_INTF_OPCODE, WLAN_INTF_OPCODE
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wlanapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - _WLAN_INTF_OPCODE
 - wlanapi/_WLAN_INTF_OPCODE
 - PWLAN_INTF_OPCODE
 - wlanapi/PWLAN_INTF_OPCODE
 - WLAN_INTF_OPCODE
 - wlanapi/WLAN_INTF_OPCODE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_INTF_OPCODE
 - WLAN_INTF_OPCODE
---

# WLAN_INTF_OPCODE enumeration


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

The opcode used to query the state of the interface. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_current_connection

The opcode used to query information about the current connection of the interface. 

This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function. If the interface is in disconnected or disconnecting state, <b>WlanQueryInterface</b> function returns <b>ERROR_INVALID_STATE</b>.

### -field wlan_intf_opcode_channel_number

The opcode used to query the current channel on which the wireless interface is operating. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs

The opcode used to query the supported auth/cipher pairs for infrastructure mode. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_supported_adhoc_auth_cipher_pairs

The opcode used to query the supported auth/cipher pairs for ad hoc mode. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_supported_country_or_region_string_list

The opcode used to query the list of supported country or region strings. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_current_operation_mode

The opcode used to set or query the current operation mode of the wireless interface. For more information about operation modes, see <a href="https://www.microsoft.com/?ref=go">Native 802.11 Operation Modes</a>.

### -field wlan_intf_opcode_supported_safe_mode

The opcode used to query whether the miniport/NIC combination supports Federal Information Processing Standards (FIPS) mode. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function. FIPS mode is also known as safe mode. This wireless safe mode is different than the operating system safe mode.

### -field wlan_intf_opcode_certified_safe_mode

The opcode used to query whether the miniport/NIC combination is FIPS certified. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_hosted_network_capable

The opcode used to query for Hosted Network support in the device driver associated with the Wireless interface. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function. 

The data type returned for this opcode by a query is a Boolean. A value returned of <b>TRUE</b> indicates Hosted Network is supported. A value of <b>FALSE</b> indicates Hosted Network is not supported. 

This value is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  on Windows Server 2008 R2 with the Wireless LAN Service installed.

### -field wlan_intf_opcode_management_frame_protection_capable

The opcode used to query whether Management Frame Protection (MFP) is supported in the device driver associated with the Wireless interface. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function. 

MFP is defined in the IEEE 802.11w-2009 amendment to 802.11 standard.

This value is supported on Windows 8 and  on Windows Server 2012.

### -field wlan_intf_opcode_autoconf_end:0x0fffffff

Not used.

### -field wlan_intf_opcode_msm_start:0x10000100

Not used.

### -field wlan_intf_opcode_statistics

The opcode used to query driver statistics. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_rssi

Opcode used to query the received signal strength. This opcode can only be used in a query operation with the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> function.

### -field wlan_intf_opcode_msm_end:0x1fffffff

Not used.

### -field wlan_intf_opcode_security_start:0x20010000

Not used.

### -field wlan_intf_opcode_security_end:0x2fffffff

Not used.

### -field wlan_intf_opcode_ihv_start:0x30000000

Not used.

### -field wlan_intf_opcode_ihv_end:0x3fffffff

## -remarks

The <b>WLAN_INTF_OPCODE</b> enumerated type defines the possible opcodes that can be passed in the <i>OpCode</i> parameter to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a> and <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a> functions to query or set parameters on a wireless interface.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a>
