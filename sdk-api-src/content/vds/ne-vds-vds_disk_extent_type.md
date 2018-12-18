---
UID: NE:vds._VDS_DISK_EXTENT_TYPE
title: VDS_DISK_EXTENT_TYPE
author: windows-sdk-content
description: Defines the set of disk extents types. The type can be a partition, volume, or free space.
old-location: base\vds_disk_extent_type.htm
tech.root: vds
ms.assetid: 3f7a5dba-315b-4757-bd4c-1335c18739eb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_DET_CLUSTER, VDS_DET_DATA, VDS_DET_ESP, VDS_DET_FREE, VDS_DET_LDM, VDS_DET_MSR, VDS_DET_OEM, VDS_DET_UNKNOWN, VDS_DET_UNUSABLE, VDS_DISK_EXTENT_TYPE, VDS_DISK_EXTENT_TYPE enumeration [VDS], base.vds_disk_extent_type, vds/VDS_DET_CLUSTER, vds/VDS_DET_DATA, vds/VDS_DET_ESP, vds/VDS_DET_FREE, vds/VDS_DET_LDM, vds/VDS_DET_MSR, vds/VDS_DET_OEM, vds/VDS_DET_UNKNOWN, vds/VDS_DET_UNUSABLE, vds/VDS_DISK_EXTENT_TYPE
ms.topic: enum
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
 - VDS_DISK_EXTENT_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_DISK_EXTENT_TYPE
req.redist: 
---

# VDS_DISK_EXTENT_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of disk extents types. The type can be a partition, volume, or free space.


## -enum-fields




### -field VDS_DET_UNKNOWN

An extent of any unknown partition.


### -field VDS_DET_FREE

An extent of free space, including free space inside an extended partition.


### -field VDS_DET_DATA

An extent of any volume.


### -field VDS_DET_OEM

An extent of an OEM partition.


### -field VDS_DET_ESP

An extent of an ESP partition.


### -field VDS_DET_MSR

An extent of a MSR partition.


### -field VDS_DET_LDM

An extent of a LDM metadata partition.


### -field VDS_DET_CLUSTER

An extent of a cluster metadata partition.


### -field VDS_DET_UNUSABLE

An extent of unusable space on a disk. That is, space outside the four primary partitions (or three primary partitions plus one extended partition) on a basic MBR disk and space outside the dynamic disk public region.


## -remarks



ESP, MBR, and LDM metadata partitions are partition styles on GPT disks only.

The <a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a> structure includes a <b>VDS_DISK_EXTENT_TYPE</b> value as a member to indicate an existing disk extent type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DISK_EXTENT_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DISK_EXTENT_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a>
 

 

