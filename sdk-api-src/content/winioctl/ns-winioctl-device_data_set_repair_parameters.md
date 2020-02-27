---
UID: NS:winioctl._DEVICE_DATA_SET_REPAIR_PARAMETERS
title: DEVICE_DATA_SET_REPAIR_PARAMETERS
description: Specifies parameters for the repair operation.
old-location: base\device_data_set_repair_parameters.htm
tech.root: devio
ms.assetid: 95bc892c-9bb7-464c-8084-7cc6e643fa28
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_DATA_SET_REPAIR_PARAMETERS, *PDEVICE_DSM_REPAIR_PARAMETERS, DEVICE_DATA_SET_REPAIR_PARAMETERS, DEVICE_DATA_SET_REPAIR_PARAMETERS structure, DEVICE_DSM_REPAIR_PARAMETERS, PDEVICE_DATA_SET_REPAIR_PARAMETERS, PDEVICE_DATA_SET_REPAIR_PARAMETERS structure pointer, base.device_data_set_repair_parameters, winioctl/DEVICE_DATA_SET_REPAIR_PARAMETERS, winioctl/PDEVICE_DATA_SET_REPAIR_PARAMETERS'
f1_keywords:
- winioctl/DEVICE_DATA_SET_REPAIR_PARAMETERS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- DEVICE_DATA_SET_REPAIR_PARAMETERS
targetos: Windows
req.typenames: DEVICE_DATA_SET_REPAIR_PARAMETERS, *PDEVICE_DATA_SET_REPAIR_PARAMETERS, DEVICE_DSM_REPAIR_PARAMETERS, *PDEVICE_DSM_REPAIR_PARAMETERS
req.redist: 
---

# DEVICE_DATA_SET_REPAIR_PARAMETERS structure


## -description


Specifies parameters for the repair operation. A repair operation is 
    initiated by specifying <b>DeviceDsmAction_Repair</b> in the 
    <b>Action</b> member of the 
    <a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    structure passed in a 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field NumberOfRepairCopies

The number of copies that will be repaired.


### -field SourceCopy

The copy number of the source copy.


### -field RepairCopies

The copy numbers of all the copies that will be repaired.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>
 

 

