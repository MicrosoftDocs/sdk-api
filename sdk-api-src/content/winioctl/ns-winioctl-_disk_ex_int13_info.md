---
UID: NS:winioctl._DISK_EX_INT13_INFO
title: "_DISK_EX_INT13_INFO"
author: windows-driver-content
description: Contains extended Int13 drive parameters.
old-location: fs\disk_ex_int13_info_str.htm
old-project: FileIO
ms.assetid: efde6ede-b921-4d1d-ab4a-b9f85ae6aea1
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PDISK_EX_INT13_INFO, DISK_EX_INT13_INFO, DISK_EX_INT13_INFO structure [Files], PDISK_EX_INT13_INFO, PDISK_EX_INT13_INFO structure pointer [Files], _DISK_EX_INT13_INFO, _win32_disk_ex_int13_info_str, base.disk_ex_int13_info_str, fs.disk_ex_int13_info_str, winioctl/DISK_EX_INT13_INFO, winioctl/PDISK_EX_INT13_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISK_EX_INT13_INFO, *PDISK_EX_INT13_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	DISK_EX_INT13_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DISK_EX_INT13_INFO structure


## -description


Contains extended Int13 drive parameters.


## -struct-fields




### -field ExBufferSize

The size of the extended drive parameter buffer for this partition or disk.  For valid values, see the BIOS documentation.


### -field ExFlags

The information flags for this partition or disk.  For valid values, see the BIOS documentation.


### -field ExCylinders

The number of cylinders per head.  For valid values, see the BIOS documentation.


### -field ExHeads

The maximum number of heads for this hard disk.  For valid values, see the BIOS documentation.


### -field ExSectorsPerTrack

The number of sectors per track.  For valid values, see the BIOS documentation.


### -field ExSectorsPerDrive

The total number of sectors for this disk.  For valid values, see the BIOS documentation.


### -field ExSectorSize

The sector size for this disk.  For valid values, see the BIOS documentation.


### -field ExReserved

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552601">DISK_DETECTION_INFO</a>
 

 

