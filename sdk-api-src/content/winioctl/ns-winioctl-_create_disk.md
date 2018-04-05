---
UID: NS:winioctl._CREATE_DISK
title: "_CREATE_DISK"
author: windows-driver-content
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.
old-location: fs\create_disk_str.htm
old-project: FileIO
ms.assetid: ec4a1ef9-ff2e-41b3-951b-241c545f256b
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PCREATE_DISK, CREATE_DISK, CREATE_DISK structure [Files], PCREATE_DISK, PCREATE_DISK structure pointer [Files], _CREATE_DISK, _win32_create_disk_str, base.create_disk_str, fs.create_disk_str, winioctl/CREATE_DISK, winioctl/PCREATE_DISK"
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
req.typenames: CREATE_DISK, *PCREATE_DISK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	CREATE_DISK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CREATE_DISK structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field PartitionStyle

The format of a partition. 

For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>.


#### - Gpt

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552486">CREATE_DISK_GPT</a> structure that contains disk information when a GPT disk is to be initialized.


#### - Mbr

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552490">CREATE_DISK_MBR</a> structure that contains disk information when an MBR disk is to be initialized.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552486">CREATE_DISK_GPT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552490">CREATE_DISK_MBR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>
 

 

