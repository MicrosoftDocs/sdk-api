---
UID: NS:winioctl._DEVICE_DATA_SET_RANGE
title: DEVICE_DATA_SET_RANGE
description: Provides data set range information for use with the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PDEVICE_DATA_SET_RANGE","*PDEVICE_DSM_RANGE","DEVICE_DATA_SET_RANGE","DEVICE_DATA_SET_RANGE structure","DEVICE_DSM_RANGE","PDEVICE_DATA_SET_RANGE","PDEVICE_DATA_SET_RANGE structure pointer","base.device_data_set_range","winioctl/DEVICE_DATA_SET_RANGE","winioctl/PDEVICE_DATA_SET_RANGE"]
old-location: base\device_data_set_range.htm
tech.root: base
ms.assetid: 5eea412e-ea16-4f47-ac69-46b543069eae
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DATA_SET_RANGE, *PDEVICE_DSM_RANGE, DEVICE_DATA_SET_RANGE, DEVICE_DATA_SET_RANGE structure, DEVICE_DSM_RANGE, PDEVICE_DATA_SET_RANGE, PDEVICE_DATA_SET_RANGE structure pointer, base.device_data_set_range, winioctl/DEVICE_DATA_SET_RANGE, winioctl/PDEVICE_DATA_SET_RANGE'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: DEVICE_DATA_SET_RANGE, *PDEVICE_DATA_SET_RANGE, DEVICE_DSM_RANGE, *PDEVICE_DSM_RANGE
req.redist: 
f1_keywords:
 - _DEVICE_DATA_SET_RANGE
 - winioctl/_DEVICE_DATA_SET_RANGE
 - PDEVICE_DATA_SET_RANGE
 - winioctl/PDEVICE_DATA_SET_RANGE
 - DEVICE_DATA_SET_RANGE
 - winioctl/DEVICE_DATA_SET_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DEVICE_DATA_SET_RANGE
---

# DEVICE_DATA_SET_RANGE structure


## -description

Provides data set range information for use with the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.

## -struct-fields

### -field StartingOffset

Starting offset of the data set range in bytes, relative to the start of the volume. Must align to disk 
      logical sector size.

### -field LengthInBytes

Length of the data set range, in bytes. Must be a multiple of disk logical sector size.

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>