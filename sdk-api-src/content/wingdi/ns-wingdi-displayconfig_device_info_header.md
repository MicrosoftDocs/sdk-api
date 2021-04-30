---
UID: NS:wingdi.DISPLAYCONFIG_DEVICE_INFO_HEADER
title: DISPLAYCONFIG_DEVICE_INFO_HEADER (wingdi.h)
description: The DISPLAYCONFIG_DEVICE_INFO_HEADER structure contains display information about the device.
helpviewer_keywords: ["CCD_Structures_b17380bb-3894-4832-bbe6-97c40607d366.xml","DISPLAYCONFIG_DEVICE_INFO_HEADER","DISPLAYCONFIG_DEVICE_INFO_HEADER structure [Display Devices]","display.displayconfig_device_info_header","wingdi/DISPLAYCONFIG_DEVICE_INFO_HEADER"]
old-location: display\displayconfig_device_info_header.htm
tech.root: display
ms.assetid: 2fdfa54e-2a5f-448f-98e3-e51ce0acaeaf
ms.date: 12/05/2018
ms.keywords: CCD_Structures_b17380bb-3894-4832-bbe6-97c40607d366.xml, DISPLAYCONFIG_DEVICE_INFO_HEADER, DISPLAYCONFIG_DEVICE_INFO_HEADER structure [Display Devices], display.displayconfig_device_info_header, wingdi/DISPLAYCONFIG_DEVICE_INFO_HEADER
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
req.typenames: DISPLAYCONFIG_DEVICE_INFO_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_DEVICE_INFO_HEADER
 - wingdi/DISPLAYCONFIG_DEVICE_INFO_HEADER
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
 - DISPLAYCONFIG_DEVICE_INFO_HEADER
---

# DISPLAYCONFIG_DEVICE_INFO_HEADER structure


## -description

The DISPLAYCONFIG_DEVICE_INFO_HEADER structure contains display information about the device.

## -struct-fields

### -field type

A <a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_device_info_type">DISPLAYCONFIG_DEVICE_INFO_TYPE</a> enumerated value that determines the type of device information to retrieve or set. The remainder of the packet for the retrieve or set operation follows immediately after the DISPLAYCONFIG_DEVICE_INFO_HEADER structure.

### -field size

The size, in bytes, of the device information that is retrieved or set. This size includes the size of the header and the size of the additional data that follows the header. This device information depends on the request type.

### -field adapterId

A locally unique identifier (LUID) that identifies the adapter that the device information packet refers to.

### -field id

The source or target identifier to get or set the device information for. The meaning of this identifier is related to the type of information being requested. For example, in the case of DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, this is the source identifier.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a> function uses the DISPLAYCONFIG_DEVICE_INFO_HEADER structure for retrieving display configuration information about the device, and the <a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a> function uses the DISPLAYCONFIG_DEVICE_INFO_HEADER structure for setting display configuration information for the device.

## -see-also

<a href="/windows/desktop/api/wingdi/ne-wingdi-displayconfig_device_info_type">DISPLAYCONFIG_DEVICE_INFO_TYPE</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfiggetdeviceinfo">DisplayConfigGetDeviceInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-displayconfigsetdeviceinfo">DisplayConfigSetDeviceInfo</a>