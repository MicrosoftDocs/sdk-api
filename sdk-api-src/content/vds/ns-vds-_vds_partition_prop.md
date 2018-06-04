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

# _VDS_PARTITION_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   properties of a partition.


## -struct-fields




### -field PartitionStyle


      The styles enumerated by <a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>. 
      The style is either master boot record (VDS_PST_MBR) or GUID partition table (VDS_PST_GPT). This member is the
      discriminant for the union.


### -field ulFlags


      The partition flags enumerated by <a href="https://msdn.microsoft.com/d6ac5769-d0bc-4a4e-93c0-e9c83303ec4c">VDS_PARTITION_FLAG</a>.
     


### -field ulPartitionNumber

The number assigned to the partition.


### -field ullOffset

The partition offset.


### -field ullSize

The size of the partition in bytes.


### -field Mbr


       If <b>PartitionStyle</b> is <b>VDS_PST_MBR</b>, MBR-specific partition 
       details. For more information see 
       <a href="https://msdn.microsoft.com/d14a852f-8a78-4631-a288-476701321ac2">VDS_PARTITION_INFO_MBR</a>.
      


### -field Gpt


       If <b>PartitionStyle</b> is <b>VDS_PST_GPT</b>, GPT-specific partition 
       details. For more information see 
       <a href="https://msdn.microsoft.com/5c484155-df73-4007-a137-998c7f1c5a7c">VDS_PARTITION_INFO_GPT</a>.


## -remarks




    The <a href="https://msdn.microsoft.com/6dc96e7b-34e5-4366-8804-d40f111d77c2">IVdsAdvancedDisk::GetPartitionProperties</a> 
    and <a href="https://msdn.microsoft.com/ca02c5f8-11cd-4bdf-a376-3b146eb2aa70">IVdsAdvancedDisk::QueryPartitions</a> 
    methods return this structure to report the property details of a partition.




## -see-also




<a href="https://msdn.microsoft.com/6dc96e7b-34e5-4366-8804-d40f111d77c2">IVdsAdvancedDisk::GetPartitionProperties</a>



<a href="https://msdn.microsoft.com/ca02c5f8-11cd-4bdf-a376-3b146eb2aa70">IVdsAdvancedDisk::QueryPartitions</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/d6ac5769-d0bc-4a4e-93c0-e9c83303ec4c">VDS_PARTITION_FLAG</a>



<a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>
 

 

