---
UID: NS:winioctl._CREATE_DISK
title: CREATE_DISK
author: windows-sdk-content
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.
old-location: fs\create_disk_str.htm
tech.root: FileIO
ms.assetid: ec4a1ef9-ff2e-41b3-951b-241c545f256b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCREATE_DISK, CREATE_DISK, CREATE_DISK structure [Files], PCREATE_DISK, PCREATE_DISK structure pointer [Files], _win32_create_disk_str, base.create_disk_str, fs.create_disk_str, winioctl/CREATE_DISK, winioctl/PCREATE_DISK"
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
 - CREATE_DISK
product: Windows
targetos: Windows
req.typenames: CREATE_DISK, *PCREATE_DISK
req.redist: 
---

# CREATE_DISK structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.


## -struct-fields




### -field PartitionStyle

The format of a partition. 

For more information, see 
<a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a>.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Mbr

A 
<a href="https://msdn.microsoft.com/6b475622-371d-4097-9de1-6ef31af76322">CREATE_DISK_MBR</a> structure that contains disk information when an MBR disk is to be initialized.


### -field DUMMYUNIONNAME.Gpt

A 
<a href="https://msdn.microsoft.com/526a265b-e15e-4cd2-adaf-c955a8cb92e5">CREATE_DISK_GPT</a> structure that contains disk information when a GPT disk is to be initialized.


## -see-also




<a href="https://msdn.microsoft.com/526a265b-e15e-4cd2-adaf-c955a8cb92e5">CREATE_DISK_GPT</a>



<a href="https://msdn.microsoft.com/6b475622-371d-4097-9de1-6ef31af76322">CREATE_DISK_MBR</a>



<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a>



<a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a>
 

 

