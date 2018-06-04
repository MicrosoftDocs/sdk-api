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

# _DISK_GROW_PARTITION structure


## -description


Contains information used to increase the size of a partition.
			This structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560376">IOCTL_DISK_GROW_PARTITION</a> control code.


## -struct-fields




### -field PartitionNumber

The identifier of the partition to be enlarged.


### -field BytesToGrow

The number of bytes by which the partition is to be enlarged (positive value) or reduced (negative value). Note that this value is not the new size of the partition.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560376">IOCTL_DISK_GROW_PARTITION</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

