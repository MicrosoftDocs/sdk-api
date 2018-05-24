---
UID: NS:vds._VDS_PARTITION_PROP
title: "_VDS_PARTITION_PROP"
author: windows-driver-content
description: Defines the properties of a partition.
old-location: base\vds_partition_prop.htm
old-project: VDS
ms.assetid: f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: VDS_PARTITION_PROP, VDS_PARTITION_PROP structure [VDS], _VDS_PARTITION_PROP, base.vds_partition_prop, vds/_VDS_PARTITION_PROP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: VDS_PARTITION_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_PARTITION_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

