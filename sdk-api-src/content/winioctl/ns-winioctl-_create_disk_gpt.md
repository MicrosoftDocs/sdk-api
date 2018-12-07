---
UID: NS:winioctl._CREATE_DISK_GPT
title: "_CREATE_DISK_GPT"
author: windows-sdk-content
description: Contains information used by the IOCTL_DISK_CREATE_DISK control code to initialize GUID partition table (GPT) disks.
old-location: fs\create_disk_gpt_str.htm
tech.root: fileio
ms.assetid: 526a265b-e15e-4cd2-adaf-c955a8cb92e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCREATE_DISK_GPT, CREATE_DISK_GPT, CREATE_DISK_GPT structure [Files], PCREATE_DISK_GPT, PCREATE_DISK_GPT structure pointer [Files], _CREATE_DISK_GPT, _win32_create_disk_gpt_str, base.create_disk_gpt_str, fs.create_disk_gpt_str, winioctl/CREATE_DISK_GPT, winioctl/PCREATE_DISK_GPT"
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
 - CREATE_DISK_GPT
product: Windows
targetos: Windows
req.typenames: CREATE_DISK_GPT, *PCREATE_DISK_GPT
req.redist: 
---

# _CREATE_DISK_GPT structure


## -description


Contains information used by the 
<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a> control code to initialize GUID partition table (GPT) disks.


## -struct-fields




### -field DiskId

The disk identifier (GUID) of the GPT disk to be initialized.


### -field MaxPartitionCount

The maximum number of partitions allowed on the GPT disk to be initialized without repartitioning the disk.
					


## -remarks



The 
<b>CREATE_DISK_GPT</b> structure is defined as part of the 
<a href="https://msdn.microsoft.com/ec4a1ef9-ff2e-41b3-951b-241c545f256b">CREATE_DISK</a> structure.

If a maximum partition count of less than 128 is specified, it will be reset to 128. This is in compliance with the EFI specification. For more information on the Extensible Firmware Interface (EFI), see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84097">Firmware and Boot Environment</a>.




## -see-also




<a href="https://msdn.microsoft.com/ec4a1ef9-ff2e-41b3-951b-241c545f256b">CREATE_DISK</a>



<a href="https://msdn.microsoft.com/6b475622-371d-4097-9de1-6ef31af76322">CREATE_DISK_MBR</a>



<a href="https://msdn.microsoft.com/c8215a00-ea39-4268-bb66-68cf3d37baef">IOCTL_DISK_CREATE_DISK</a>
 

 

