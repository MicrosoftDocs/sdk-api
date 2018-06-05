---
UID: NS:vds._VDS_PARTITION_INFO_MBR
title: "_VDS_PARTITION_INFO_MBR"
author: windows-sdk-content
description: Defines the details of a master boot record (MBR) partition.
old-location: base\vds_partition_info_mbr.htm
old-project: VDS
ms.assetid: d14a852f-8a78-4631-a288-476701321ac2
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_PARTITION_INFO_MBR, VDS_PARTITION_INFO_MBR structure [VDS], _VDS_PARTITION_INFO_MBR, base.vds_partition_info_mbr, vds/_VDS_PARTITION_INFO_MBR
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_PARTITION_INFO_MBR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_PARTITION_INFO_MBR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_PARTITION_INFO_MBR structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of a master boot record (MBR) partition.


## -struct-fields




### -field partitionType

Byte value indicating the partition type.


### -field bootIndicator

If true, the partition is active and can be booted; otherwise, the partition cannot be used to boot the computer.


### -field recognizedPartition

If true, the operating system recognizes the partition style; otherwise, the partition style is unknown.


### -field hiddenSectors

Reserved sectors.


## -remarks



This structure is used in the <b>Mbr</b> member of the <a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a> structure.

For information about partition types, see <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>



<a href="https://msdn.microsoft.com/5c484155-df73-4007-a137-998c7f1c5a7c">VDS_PARTITION_INFO_GPT</a>
 

 

