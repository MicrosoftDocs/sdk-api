---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_SLOT_INFO
title: "_STORAGE_HW_FIRMWARE_SLOT_INFO"
author: windows-driver-content
description: This structure contains information about a slot on a device.
old-location: fs\storage_hw_firmware_slot_info.htm
old-project: FileIO
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PSTORAGE_HW_FIRMWARE_SLOT_INFO, PSTORAGE_HW_FIRMWARE_SLOT_INFO, PSTORAGE_HW_FIRMWARE_SLOT_INFO structure pointer [Files], STORAGE_HW_FIRMWARE_SLOT_INFO, STORAGE_HW_FIRMWARE_SLOT_INFO structure [Files], _STORAGE_HW_FIRMWARE_SLOT_INFO, fs.storage_hw_firmware_slot_info, winioctl/PSTORAGE_HW_FIRMWARE_SLOT_INFO, winioctl/STORAGE_HW_FIRMWARE_SLOT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winioctl.h.h
api_name:
-	STORAGE_HW_FIRMWARE_SLOT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_HW_FIRMWARE_SLOT_INFO structure


## -description


This structure contains information about a slot on a device.


## -struct-fields




### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_SLOT_INFO)


### -field Size

The size of this structure.


### -field SlotNumber

The slot number of this slot.


### -field ReadOnly

Indicates whether this slot is read-only or not.


### -field Reserved0

Reserved for future use.


### -field Reserved1

Reserved for future use.


### -field Revision

The revision of the firmware on this slot.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn932065">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932066">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932067">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931808">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931809">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931810">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931811">STORAGE_HW_FIRMWARE_INFO_QUERY</a>
 

 

