---
UID: NS:wingdi.DISPLAYCONFIG_TARGET_DEVICE_NAME
title: DISPLAYCONFIG_TARGET_DEVICE_NAME (wingdi.h)
description: The DISPLAYCONFIG_TARGET_DEVICE_NAME structure contains information about the target.
helpviewer_keywords: ["CCD_Structures_71e42f61-634a-47fe-b330-404dbe59e211.xml","DISPLAYCONFIG_TARGET_DEVICE_NAME","DISPLAYCONFIG_TARGET_DEVICE_NAME structure [Display Devices]","display.displayconfig_target_device_name","wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME"]
old-location: display\displayconfig_target_device_name.htm
tech.root: display
ms.assetid: 85507b69-8ce0-4f39-a4d3-7d67f515b451
ms.date: 12/05/2018
ms.keywords: CCD_Structures_71e42f61-634a-47fe-b330-404dbe59e211.xml, DISPLAYCONFIG_TARGET_DEVICE_NAME, DISPLAYCONFIG_TARGET_DEVICE_NAME structure [Display Devices], display.displayconfig_target_device_name, wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME
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
req.typenames: DISPLAYCONFIG_TARGET_DEVICE_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_TARGET_DEVICE_NAME
 - wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME
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
 - DISPLAYCONFIG_TARGET_DEVICE_NAME
---

# DISPLAYCONFIG_TARGET_DEVICE_NAME structure


## -description

The DISPLAYCONFIG_TARGET_DEVICE_NAME structure contains information about the target.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the target device name. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME and the <b>adapterId</b> and <b>id</b> members of DISPLAYCONFIG_DEVICE_INFO_HEADER to the target for which the caller wants the target device name. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_TARGET_DEVICE_NAME structure.

### -field flags

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name_flags">DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</a> structure that identifies, in bit-field flags, information about the target.

### -field outputTechnology

A value from the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a> enumeration that specifies the target's connector type.

### -field edidManufactureId

 The manufacture identifier from the monitor extended display identification data (EDID). This member is set only when the <b>edidIdsValid</b> bit-field is set in the <b>flags</b> member.

### -field edidProductCodeId

 The product code from the monitor EDID. This member is set only when the <b>edidIdsValid</b> bit-field is set in the <b>flags</b> member.

### -field connectorInstance

The one-based instance number of this particular target only when the adapter has multiple targets of this type. The connector instance is a consecutive one-based number that is unique within each adapter. If this is the only target of this type on the adapter, this value is zero.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^

### -field monitorFriendlyDeviceName

A NULL-terminated WCHAR string that is the  device name for the monitor. This name can be used with <i>SetupAPI.dll</i> to obtain the device name that is contained in the installation package.

### -field monitorDevicePath

A NULL-terminated WCHAR string that is the  path to the device name for the monitor. This path can be used with <i>SetupAPI.dll</i> to obtain the device name that is contained in the installation package.

## -remarks

Extended display identification data (EDID) is a set of data that is provided by a display to describe its capabilities to a graphics adapter. EDID data allows a computer to detect the type of monitor that is connected to it. EDID data includes the manufacturer name, the product type, the timings that are supported by the display, the display size, as well as other display characteristics. EDID is defined by a standard published by the Video Electronics Standards Association (VESA).

A named device object has a path and name of the form <i>\Device\DeviceName</i>. This is known as the <i>device name</i> of the device object.

If an application calls the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function to obtain the monitor name and <b>DisplayConfigGetDeviceInfo</b> either cannot get the monitor name or the target is forced without a monitor connected, the string in the <b>monitorFriendlyDeviceName</b> member of the DISPLAYCONFIG_TARGET_DEVICE_NAME structure is a <b>NULL</b> string and none of the bit-field flags in the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name_flags">DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</a> structure are set.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name_flags">DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>
