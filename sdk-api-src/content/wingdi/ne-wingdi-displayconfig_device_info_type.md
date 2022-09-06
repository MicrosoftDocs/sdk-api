---
UID: NE:wingdi.__unnamed_enum_6
title: DISPLAYCONFIG_DEVICE_INFO_TYPE (wingdi.h)
description: The DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration specifies the type of display device info to configure or obtain through the DisplayConfigSetDeviceInfo or DisplayConfigGetDeviceInfo function.
helpviewer_keywords: ["CCD_Enumerations_29e89f4b-f002-4493-a1dc-5dba3150a7f8.xml","DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32","DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME","DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME","DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION","DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE","DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME","DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE","DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION","DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE","DISPLAYCONFIG_DEVICE_INFO_TYPE","DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration [Display Devices]","display.displayconfig_device_info_type","wingdi/DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME","wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE","wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION","wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE","wingdi/DISPLAYCONFIG_DEVICE_INFO_TYPE"]
old-location: display\displayconfig_device_info_type.htm
tech.root: display
ms.assetid: 40cc67c0-1508-4b67-b297-5a8dabaabb16
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_29e89f4b-f002-4493-a1dc-5dba3150a7f8.xml, DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32, DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE, DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION, DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE, DISPLAYCONFIG_DEVICE_INFO_TYPE, DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration [Display Devices], display.displayconfig_device_info_type, wingdi/DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE, wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION, wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE, wingdi/DISPLAYCONFIG_DEVICE_INFO_TYPE
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
req.target-min-winversvr: 
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
req.typenames: DISPLAYCONFIG_DEVICE_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_DEVICE_INFO_TYPE
 - wingdi/DISPLAYCONFIG_DEVICE_INFO_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_DEVICE_INFO_TYPE
---

# DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration


## -description

The DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration specifies the type of display device info to configure or obtain through the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a> or <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function.

## -enum-fields

### -field DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME:1

Specifies the source name of the display device. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns the source name in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_source_device_name">DISPLAYCONFIG_SOURCE_DEVICE_NAME</a> structure.

### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME:2

Specifies information about the monitor. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns info about the monitor in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure.

### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE:3

Specifies information about the preferred mode of a monitor. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns info about the preferred mode of a monitor in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_preferred_mode">DISPLAYCONFIG_TARGET_PREFERRED_MODE</a> structure.

### -field DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME:4

Specifies the graphics adapter name. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns the adapter name in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_adapter_name">DISPLAYCONFIG_ADAPTER_NAME</a> structure.

### -field DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE:5

Specifies how to set the monitor. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a> function is successful, <b>DisplayConfigSetDeviceInfo</b> uses info in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_set_target_persistence">DISPLAYCONFIG_SET_TARGET_PERSISTENCE</a> structure to force the output in a boot-persistent manner.

### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE:6

Specifies how to set the base output technology for a given target ID. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns base output technology info in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_base_type">DISPLAYCONFIG_TARGET_BASE_TYPE</a> structure.

Supported by WDDM 1.3 and later user-mode display drivers running on Windows 8.1 and later.

### -field DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION:7

Specifies the state of virtual mode support. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns virtual mode support information in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_support_virtual_resolution">DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION</a> structure. Supported starting in Windows 10.

### -field DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION:8

Specifies how to set the state of virtual mode support. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a> function is successful, <b>DisplayConfigSetDeviceInfo</b> uses info in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_support_virtual_resolution">DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION</a> structure to change the state of virtual mode support. Supported starting in Windows 10.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_ADVANCED_COLOR_INFO:9

### -field DISPLAYCONFIG_DEVICE_INFO_SET_ADVANCED_COLOR_STATE:10

### -field DISPLAYCONFIG_DEVICE_INFO_GET_SDR_WHITE_LEVEL:11

Specifies the current SDR white level for an HDR monitor. If the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> return SDR white level info in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_sdr_white_level">DISPLAYCONFIG_SDR_WHITE_LEVEL</a> structure.

Supported starting in Windows�10 Fall Creators Update (Version 1709).


### -field DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_adapter_name">DISPLAYCONFIG_ADAPTER_NAME</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_set_target_persistence">DISPLAYCONFIG_SET_TARGET_PERSISTENCE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_source_device_name">DISPLAYCONFIG_SOURCE_DEVICE_NAME</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_base_type">DISPLAYCONFIG_TARGET_BASE_TYPE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_preferred_mode">DISPLAYCONFIG_TARGET_PREFERRED_MODE</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a>
