---
UID: NS:wingdi.DISPLAYCONFIG_SOURCE_DEVICE_NAME
title: DISPLAYCONFIG_SOURCE_DEVICE_NAME (wingdi.h)
description: The DISPLAYCONFIG_SOURCE_DEVICE_NAME structure contains the GDI device name for the source or view.
helpviewer_keywords: ["CCD_Structures_0a443841-294d-4b14-8f95-7825de89b8ac.xml","DISPLAYCONFIG_SOURCE_DEVICE_NAME","DISPLAYCONFIG_SOURCE_DEVICE_NAME structure [Display Devices]","display.displayconfig_source_device_name","wingdi/DISPLAYCONFIG_SOURCE_DEVICE_NAME"]
old-location: display\displayconfig_source_device_name.htm
tech.root: display
ms.assetid: 92813ffc-1915-4f26-afb1-936bf76f7844
ms.date: 12/05/2018
ms.keywords: CCD_Structures_0a443841-294d-4b14-8f95-7825de89b8ac.xml, DISPLAYCONFIG_SOURCE_DEVICE_NAME, DISPLAYCONFIG_SOURCE_DEVICE_NAME structure [Display Devices], display.displayconfig_source_device_name, wingdi/DISPLAYCONFIG_SOURCE_DEVICE_NAME
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
req.typenames: DISPLAYCONFIG_SOURCE_DEVICE_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_SOURCE_DEVICE_NAME
 - wingdi/DISPLAYCONFIG_SOURCE_DEVICE_NAME
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
 - DISPLAYCONFIG_SOURCE_DEVICE_NAME
---

# DISPLAYCONFIG_SOURCE_DEVICE_NAME structure


## -description

The <b>DISPLAYCONFIG_SOURCE_DEVICE_NAME</b> structure contains the GDI device name for the source or view.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the source device name. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME and the <b>adapterId</b> and <b>id</b> members of DISPLAYCONFIG_DEVICE_INFO_HEADER to the source for which the caller wants the source device name. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_SOURCE_DEVICE_NAME structure.

### -field viewGdiDeviceName

A NULL-terminated WCHAR string that is the GDI device name for the source, or view. This name can be used in a call to <b>EnumDisplaySettings</b> to obtain a list of available modes for the specified source.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>