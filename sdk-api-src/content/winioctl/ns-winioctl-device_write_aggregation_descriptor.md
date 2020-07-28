---
UID: NS:winioctl._DEVICE_WRITE_AGGREGATION_DESCRIPTOR
title: DEVICE_WRITE_AGGREGATION_DESCRIPTOR
description: Reserved for system use.
helpviewer_keywords: ["*PDEVICE_WRITE_AGGREGATION_DESCRIPTOR","DEVICE_WRITE_AGGREGATION_DESCRIPTOR","DEVICE_WRITE_AGGREGATION_DESCRIPTOR structure [Files]","PDEVICE_WRITE_AGGREGATION_DESCRIPTOR","PDEVICE_WRITE_AGGREGATION_DESCRIPTOR structure pointer [Files]","fs.device_write_aggregation_descriptor","winioctl/DEVICE_WRITE_AGGREGATION_DESCRIPTOR","winioctl/PDEVICE_WRITE_AGGREGATION_DESCRIPTOR"]
old-location: fs\device_write_aggregation_descriptor.htm
tech.root: fs
ms.assetid: 124f05bc-6c3f-4778-9cc0-5a55891cb141
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_WRITE_AGGREGATION_DESCRIPTOR, DEVICE_WRITE_AGGREGATION_DESCRIPTOR, DEVICE_WRITE_AGGREGATION_DESCRIPTOR structure [Files], PDEVICE_WRITE_AGGREGATION_DESCRIPTOR, PDEVICE_WRITE_AGGREGATION_DESCRIPTOR structure pointer [Files], fs.device_write_aggregation_descriptor, winioctl/DEVICE_WRITE_AGGREGATION_DESCRIPTOR, winioctl/PDEVICE_WRITE_AGGREGATION_DESCRIPTOR'
f1_keywords:
- winioctl/DEVICE_WRITE_AGGREGATION_DESCRIPTOR
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- DEVICE_WRITE_AGGREGATION_DESCRIPTOR
targetos: Windows
req.typenames: DEVICE_WRITE_AGGREGATION_DESCRIPTOR, *PDEVICE_WRITE_AGGREGATION_DESCRIPTOR
req.redist: 
---

# DEVICE_WRITE_AGGREGATION_DESCRIPTOR structure


## -description


Reserved for system use.


## -struct-fields




### -field Version

Contains the size, in bytes, of this structure. The value of this member will change as members are added 
      to the structure.


### -field Size

Specifies the total size of the descriptor, in bytes.


### -field BenefitsFromWriteAggregation

<b>TRUE</b> if the device benefits from write aggregation.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>
 

 

