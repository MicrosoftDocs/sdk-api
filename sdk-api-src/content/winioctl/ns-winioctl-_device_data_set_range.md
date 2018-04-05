---
UID: NS:winioctl._DEVICE_DATA_SET_RANGE
title: "_DEVICE_DATA_SET_RANGE"
author: windows-driver-content
description: Provides data set range information for use with the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
old-location: base\device_data_set_range.htm
old-project: DevIO
ms.assetid: 5eea412e-ea16-4f47-ac69-46b543069eae
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PDEVICE_DATA_SET_RANGE, DEVICE_DATA_SET_RANGE, DEVICE_DATA_SET_RANGE structure, PDEVICE_DATA_SET_RANGE, PDEVICE_DATA_SET_RANGE structure pointer, _DEVICE_DATA_SET_RANGE, base.device_data_set_range, winioctl/DEVICE_DATA_SET_RANGE, winioctl/PDEVICE_DATA_SET_RANGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DEVICE_DATA_SET_RANGE, *PDEVICE_DATA_SET_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	DEVICE_DATA_SET_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DEVICE_DATA_SET_RANGE structure


## -description


Provides data set range information for use with the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field StartingOffset

Starting offset of the data set range in bytes, relative to the start of the volume. Must align to disk 
      logical sector size.


### -field LengthInBytes

Length of the data set range, in bytes. Must be a multiple of disk logical sector size.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>
 

 

