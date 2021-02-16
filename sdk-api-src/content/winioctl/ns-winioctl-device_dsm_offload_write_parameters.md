---
UID: NS:winioctl._DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
title: DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
description: Specifies parameters for the offload write operation.
helpviewer_keywords: ["*PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS","DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS","DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure","PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS","PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure pointer","base.device_dsm_offload_write_parameters","winioctl/DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS","winioctl/PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS"]
old-location: base\device_dsm_offload_write_parameters.htm
tech.root: base
ms.assetid: d0107cae-50c9-46d2-97cd-324030692903
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure, PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure pointer, base.device_dsm_offload_write_parameters, winioctl/DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, winioctl/PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS'
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
req.typenames: DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, *PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
req.redist: 
f1_keywords:
 - _DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
 - winioctl/_DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
 - PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
 - winioctl/PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
 - DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
 - winioctl/DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
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
 - DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
---

# DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure


## -description

Specifies parameters for the offload write operation. An offload write operation is 
    initiated by specifying <b>DeviceDsmAction_OffloadWrite</b> in the 
    <b>Action</b> member of the 
    <a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    structure passed in a 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.

## -struct-fields

### -field Flags

Set to 0.

### -field Reserved

Reserved.

### -field TokenOffset

The starting offset to copy from the range bound to the token

### -field Token

<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_token">STORAGE_OFFLOAD_TOKEN</a> structure containing 
      the token returned from the offload read operation.

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_token">STORAGE_OFFLOAD_TOKEN</a>