---
UID: NS:winioctl._DEVICE_DSM_OFFLOAD_READ_PARAMETERS
title: DEVICE_DSM_OFFLOAD_READ_PARAMETERS
description: Contains parameters for the DeviceDsmAction_OffloadRead action for the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PDEVICE_DSM_OFFLOAD_READ_PARAMETERS","DEVICE_DSM_OFFLOAD_READ_PARAMETERS","DEVICE_DSM_OFFLOAD_READ_PARAMETERS structure","PDEVICE_DSM_OFFLOAD_READ_PARAMETERS","PDEVICE_DSM_OFFLOAD_READ_PARAMETERS structure pointer","base.device_dsm_offload_read_parameters","winioctl/DEVICE_DSM_OFFLOAD_READ_PARAMETERS","winioctl/PDEVICE_DSM_OFFLOAD_READ_PARAMETERS"]
old-location: base\device_dsm_offload_read_parameters.htm
tech.root: base
ms.assetid: 20dd3e5b-90f4-45fc-8cc8-bf9e6d08a026
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DSM_OFFLOAD_READ_PARAMETERS, DEVICE_DSM_OFFLOAD_READ_PARAMETERS, DEVICE_DSM_OFFLOAD_READ_PARAMETERS structure, PDEVICE_DSM_OFFLOAD_READ_PARAMETERS, PDEVICE_DSM_OFFLOAD_READ_PARAMETERS structure pointer, base.device_dsm_offload_read_parameters, winioctl/DEVICE_DSM_OFFLOAD_READ_PARAMETERS, winioctl/PDEVICE_DSM_OFFLOAD_READ_PARAMETERS'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: DEVICE_DSM_OFFLOAD_READ_PARAMETERS, *PDEVICE_DSM_OFFLOAD_READ_PARAMETERS
req.redist: 
f1_keywords:
 - _DEVICE_DSM_OFFLOAD_READ_PARAMETERS
 - winioctl/_DEVICE_DSM_OFFLOAD_READ_PARAMETERS
 - PDEVICE_DSM_OFFLOAD_READ_PARAMETERS
 - winioctl/PDEVICE_DSM_OFFLOAD_READ_PARAMETERS
 - DEVICE_DSM_OFFLOAD_READ_PARAMETERS
 - winioctl/DEVICE_DSM_OFFLOAD_READ_PARAMETERS
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
 - DEVICE_DSM_OFFLOAD_READ_PARAMETERS
---

# DEVICE_DSM_OFFLOAD_READ_PARAMETERS structure


## -description

Contains parameters for the <b>DeviceDsmAction_OffloadRead</b> action for the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.

## -struct-fields

### -field Flags

Set to 0.

### -field TimeToLive

The time to live (TTL) for the token, in milliseconds.

### -field Reserved

Set to 0.

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_read_output">STORAGE_OFFLOAD_READ_OUTPUT</a>