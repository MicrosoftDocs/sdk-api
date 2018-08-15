---
UID: NS:winioctl._DEVICE_DATA_SET_REPAIR_PARAMETERS
title: "_DEVICE_DATA_SET_REPAIR_PARAMETERS"
author: windows-sdk-content
description: Specifies parameters for the repair operation.
old-location: base\device_data_set_repair_parameters.htm
old-project: devio
ms.assetid: 95bc892c-9bb7-464c-8084-7cc6e643fa28
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PDEVICE_DATA_SET_REPAIR_PARAMETERS, *PDEVICE_DSM_REPAIR_PARAMETERS, DEVICE_DATA_SET_REPAIR_PARAMETERS, DEVICE_DATA_SET_REPAIR_PARAMETERS structure, DEVICE_DSM_REPAIR_PARAMETERS, PDEVICE_DATA_SET_REPAIR_PARAMETERS, PDEVICE_DATA_SET_REPAIR_PARAMETERS structure pointer, _DEVICE_DATA_SET_REPAIR_PARAMETERS, base.device_data_set_repair_parameters, winioctl/DEVICE_DATA_SET_REPAIR_PARAMETERS, winioctl/PDEVICE_DATA_SET_REPAIR_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: DEVICE_DATA_SET_REPAIR_PARAMETERS, *PDEVICE_DATA_SET_REPAIR_PARAMETERS, DEVICE_DSM_REPAIR_PARAMETERS, *PDEVICE_DSM_REPAIR_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DEVICE_DATA_SET_REPAIR_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DEVICE_DATA_SET_REPAIR_PARAMETERS structure


## -description


Specifies parameters for the repair operation. A repair operation is 
    initiated by specifying <b>DeviceDsmAction_Repair</b> in the 
    <b>Action</b> member of the 
    <a href="https://msdn.microsoft.com/328902b7-97e3-40dc-9771-f5e64ccf3364">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    structure passed in a 
    <a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field NumberOfRepairCopies

The number of copies that will be repaired.


### -field SourceCopy

The copy number of the source copy.


### -field RepairCopies

The copy numbers of all the copies that will be repaired.


## -see-also




<a href="https://msdn.microsoft.com/328902b7-97e3-40dc-9771-f5e64ccf3364">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>
 

 

