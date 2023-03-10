---
UID: NS:wingdi.DISPLAYCONFIG_TARGET_BASE_TYPE
title: DISPLAYCONFIG_TARGET_BASE_TYPE (wingdi.h)
description: Specifies base output technology info for a given target ID.
helpviewer_keywords: ["DISPLAYCONFIG_TARGET_BASE_TYPE","DISPLAYCONFIG_TARGET_BASE_TYPE structure [Display Devices]","display.displayconfig_target_base_type","wingdi/DISPLAYCONFIG_TARGET_BASE_TYPE"]
old-location: display\displayconfig_target_base_type.htm
tech.root: display
ms.assetid: 7916E714-9A3C-4682-AC08-9B6EE222D8B7
ms.date: 12/05/2018
ms.keywords: DISPLAYCONFIG_TARGET_BASE_TYPE, DISPLAYCONFIG_TARGET_BASE_TYPE structure [Display Devices], display.displayconfig_target_base_type, wingdi/DISPLAYCONFIG_TARGET_BASE_TYPE
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: DISPLAYCONFIG_TARGET_BASE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_TARGET_BASE_TYPE
 - wingdi/DISPLAYCONFIG_TARGET_BASE_TYPE
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
 - DISPLAYCONFIG_TARGET_BASE_TYPE
---

# DISPLAYCONFIG_TARGET_BASE_TYPE structure


## -description

Specifies base output technology info for a given target ID.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains info about the request for the target device name. The caller should set the <b>type</b> member of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to <b>DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE</b> and the <b>adapterId</b> and <b>id</b> members of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to the target for which the caller wants the target device name.

 The caller should set the <b>size</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> to at least the size of the <b>DISPLAYCONFIG_TARGET_BASE_TYPE</b> structure.

### -field baseOutputTechnology

The base output technology, given as a constant value of the <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a> enumeration, of the adapter and the target specified by the <b>header</b> member. See Remarks.

## -remarks

For a Miracast display device, a call to the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>  function always returns  a value of <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>.<b>DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST</b>, regardless of what the Miracast sink reports as the connector type.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_video_output_technology">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>