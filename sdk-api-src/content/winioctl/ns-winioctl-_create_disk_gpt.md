---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CREATE_DISK_GPT structure


## -description


Contains information used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a> control code to initialize GUID partition table (GPT) disks.


## -struct-fields




### -field DiskId

The disk identifier (GUID) of the GPT disk to be initialized.


### -field MaxPartitionCount

The maximum number of partitions allowed on the GPT disk to be initialized without repartitioning the disk.
					


## -remarks



The 
<b>CREATE_DISK_GPT</b> structure is defined as part of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552484">CREATE_DISK</a> structure.

If a maximum partition count of less than 128 is specified, it will be reset to 128. This is in compliance with the EFI specification. For more information on the Extensible Firmware Interface (EFI), see 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn614600">Firmware and Boot Environment</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552484">CREATE_DISK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552490">CREATE_DISK_MBR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559436">IOCTL_DISK_CREATE_DISK</a>
 

 

