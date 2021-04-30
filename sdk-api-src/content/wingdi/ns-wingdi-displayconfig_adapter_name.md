---
UID: NS:wingdi.DISPLAYCONFIG_ADAPTER_NAME
title: DISPLAYCONFIG_ADAPTER_NAME (wingdi.h)
description: The DISPLAYCONFIG_ADAPTER_NAME structure contains information about the display adapter.
helpviewer_keywords: ["CCD_Structures_28b93049-b681-490b-a746-688f26b2fac8.xml","DISPLAYCONFIG_ADAPTER_NAME","DISPLAYCONFIG_ADAPTER_NAME structure [Display Devices]","display.displayconfig_adapter_name","wingdi/DISPLAYCONFIG_ADAPTER_NAME"]
old-location: display\displayconfig_adapter_name.htm
tech.root: display
ms.assetid: 248f325f-37ae-48f4-a758-ee78a3e3f0b8
ms.date: 12/05/2018
ms.keywords: CCD_Structures_28b93049-b681-490b-a746-688f26b2fac8.xml, DISPLAYCONFIG_ADAPTER_NAME, DISPLAYCONFIG_ADAPTER_NAME structure [Display Devices], display.displayconfig_adapter_name, wingdi/DISPLAYCONFIG_ADAPTER_NAME
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
req.typenames: DISPLAYCONFIG_ADAPTER_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_ADAPTER_NAME
 - wingdi/DISPLAYCONFIG_ADAPTER_NAME
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
 - DISPLAYCONFIG_ADAPTER_NAME
---

# DISPLAYCONFIG_ADAPTER_NAME structure


## -description

The DISPLAYCONFIG_ADAPTER_NAME structure contains information about the display adapter.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the adapter name. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME and the <b>adapterId</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to the adapter identifier of the adapter for which the caller wants the name. For this request, the caller does not need to set the <b>id</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_ADAPTER_NAME structure.

### -field adapterDevicePath

A NULL-terminated WCHAR string that is the  device name for the adapter. This name can be used with <i>SetupAPI.dll</i> to obtain the device name that is contained in the installation package.