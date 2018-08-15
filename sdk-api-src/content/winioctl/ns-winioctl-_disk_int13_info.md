---
UID: NS:winioctl._DISK_INT13_INFO
title: "_DISK_INT13_INFO"
author: windows-sdk-content
description: Contains standard Int13 drive geometry parameters.
old-location: fs\disk_int13_info_str.htm
old-project: fileio
ms.assetid: a6991ad1-da8a-4df6-a055-ead3c30938df
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDISK_INT13_INFO, DISK_INT13_INFO, DISK_INT13_INFO structure [Files], PDISK_INT13_INFO, PDISK_INT13_INFO structure pointer [Files], _DISK_INT13_INFO, _win32_disk_int13_info_str, base.disk_int13_info_str, fs.disk_int13_info_str, winioctl/DISK_INT13_INFO, winioctl/PDISK_INT13_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: DISK_INT13_INFO, *PDISK_INT13_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DISK_INT13_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DISK_INT13_INFO structure


## -description


Contains standard Int13 drive geometry parameters.


## -struct-fields




### -field DriveSelect

The letter that is related to the specified partition or hard disk.  For valid values, see the BIOS documentation.


### -field MaxCylinders

The maximum number of cylinders per head. For valid values, see the BIOS documentation.


### -field SectorsPerTrack

The number of sectors per track. For valid values, see the BIOS documentation.


### -field MaxHeads

The maximum number of heads for this hard disk.  For valid values, see the BIOS documentation.


### -field NumberDrives

The number of drives. For valid values, see the BIOS documentation.


## -see-also




<a href="https://msdn.microsoft.com/57ca68f4-f748-4bc4-90c3-13d545716d87">DISK_DETECTION_INFO</a>
 

 

