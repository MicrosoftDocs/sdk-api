---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_INFO
title: "_STORAGE_HW_FIRMWARE_INFO"
author: windows-driver-content
description: This structure contains information about the device firmware.
old-location: fs\storage_hw_firmware_info.htm
old-project: FileIO
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PSTORAGE_HW_FIRMWARE_INFO, PSTORAGE_HW_FIRMWARE_INFO, PSTORAGE_HW_FIRMWARE_INFO structure pointer [Files], STORAGE_HW_FIRMWARE_INFO, STORAGE_HW_FIRMWARE_INFO structure [Files], _STORAGE_HW_FIRMWARE_INFO, fs.storage_hw_firmware_info, winioctl/PSTORAGE_HW_FIRMWARE_INFO, winioctl/STORAGE_HW_FIRMWARE_INFO"
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
req.typenames: STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winioctl.h.h
api_name:
-	STORAGE_HW_FIRMWARE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_HW_FIRMWARE_INFO structure


## -description


This structure contains information about the device firmware.


## -struct-fields




### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_INFO)


### -field Size

The size of this structure as a buffer including slot.


### -field SupportUpgrade

Indicates that this firmware supports an upgrade.


### -field Reserved0

Reserved for future use.


### -field SlotCount

The number of firmware slots on the device. This is the dimension of the Slot array. 

<div class="alert"><b>Note</b>  Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</div>
<div> </div>

### -field ActiveSlot

The firmware slot containing the currently active/running firmware image.


### -field PendingActivateSlot

The firmware slot that is pending activation.


### -field FirmwareShared

Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.


### -field Reserved

Reserved for future use.


### -field ImagePayloadAlignment

The alignment of the image payload, in number of bytes. The maximum is PAGE_SIZE. The transfer size is a mutliple of this size. Some protocols require at least sector size. When this value is set to 0, this means that this value is invalid.


### -field ImagePayloadMaxSize

The image payload maximum size, this is used for a single command.


### -field Slot

Contains the slot information for each slot on the device, of type <a href="https://msdn.microsoft.com/library/windows/hardware/dn931812">STORAGE_HW_FIRMWARE_SLOT_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn932065">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932066">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932067">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931808">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931809">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931811">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931812">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

