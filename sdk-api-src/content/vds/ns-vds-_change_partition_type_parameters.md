---
UID: NS:vds._CHANGE_PARTITION_TYPE_PARAMETERS
title: "_CHANGE_PARTITION_TYPE_PARAMETERS"
author: windows-sdk-content
description: Describes parameters to be used when changing a partition's type.
old-location: base\change_partition_type_parameters.htm
tech.root: VDS
ms.assetid: bd51c2a6-ab26-4a2f-89f4-431d05f3dd81
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CHANGE_PARTITION_TYPE_PARAMETERS, CHANGE_PARTITION_TYPE_PARAMETERS structure, PCHANGE_PARTITION_TYPE_PARAMETERS, PCHANGE_PARTITION_TYPE_PARAMETERS structure pointer, _CHANGE_PARTITION_TYPE_PARAMETERS, base.change_partition_type_parameters, vds/CHANGE_PARTITION_TYPE_PARAMETERS, vds/PCHANGE_PARTITION_TYPE_PARAMETERS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CHANGE_PARTITION_TYPE_PARAMETERS
product: Windows
targetos: Windows
req.typenames: CHANGE_PARTITION_TYPE_PARAMETERS
req.redist: 
---

# _CHANGE_PARTITION_TYPE_PARAMETERS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Describes parameters to be used when changing a partition's type.


## -struct-fields




### -field style

A value from the <a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a> enumeration that describes the disk's partition style.


### -field MbrPartInfo

Contains information for a Master Boot Record partition.


### -field MbrPartInfo.partitionType

Byte value indicating the partition type to which to change the partition.


### -field GptPartInfo

Contains information for a GUID Partitioning Table partition.


### -field GptPartInfo.partitionType

 GUID indicating the partition type to which to change the partition.

<div class="alert"><b>Note</b>  Only the basic data partition type is allowed.</div>
<div> </div>

## -remarks



For information about partition types, see <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://msdn.microsoft.com/808a1e5a-d225-4b74-9764-3ad8cdc52ebe">IVdsAdvancedDisk2::ChangePartitionType</a>
 

 

