---
UID: NS:vds._VDS_PARTITION_INFO_GPT
title: "_VDS_PARTITION_INFO_GPT"
author: windows-sdk-content
description: Defines details of a GUID partition table (GPT) partition.
old-location: base\vds_partition_info_gpt.htm
tech.root: vds
ms.assetid: 5c484155-df73-4007-a137-998c7f1c5a7c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: VDS_PARTITION_INFO_GPT, VDS_PARTITION_INFO_GPT structure [VDS], _VDS_PARTITION_INFO_GPT, base.vds_partition_info_gpt, vds/_VDS_PARTITION_INFO_GPT
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_PARTITION_INFO_GPT
product: Windows
targetos: Windows
req.typenames: VDS_PARTITION_INFO_GPT
req.redist: 
---

# _VDS_PARTITION_INFO_GPT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines details of a GUID partition table (GPT) partition.


## -struct-fields




### -field partitionType

GUID for the partition type.


### -field partitionId

GUID for the partition.


### -field attributes

Attributes of the partition.


### -field name

Name of the partition.


## -remarks



This structure is used in the <b>Gpt</b> member of the <a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a> structure.

 A GPT table is sector-aligned.

For information about partition types and attributes, see <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>



<a href="https://msdn.microsoft.com/d14a852f-8a78-4631-a288-476701321ac2">VDS_PARTITION_INFO_MBR</a>
 

 

