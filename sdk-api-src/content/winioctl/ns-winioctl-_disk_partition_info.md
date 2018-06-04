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

# _DISK_PARTITION_INFO structure


## -description


Contains the disk partition information.


## -struct-fields




### -field SizeOfPartitionInfo

The size of this structure, in bytes.


### -field PartitionStyle

The format of a partition.

For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Mbr

If <b>PartitionStyle</b> is <b>PARTITION_STYLE_MBR</b> (0), the union 
        is a structure that contains information for an master boot record partition, which includes a disk signature 
        and a checksum.


### -field DUMMYUNIONNAME.Mbr.Signature

MBR signature of the partition.


### -field DUMMYUNIONNAME.Mbr.CheckSum

 


### -field DUMMYUNIONNAME.Gpt

If <b>PartitionStyle</b> is <b>PARTITION_STYLE_GPT</b> (1), the union 
        is a structure that contains information for a <b>GUID</b> partition table partition, 
        which includes a disk identifier (<b>GUID</b>).


### -field DUMMYUNIONNAME.Gpt.DiskId

<b>GUID</b> of the GPT partition.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552618">DISK_GEOMETRY_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>
 

 

