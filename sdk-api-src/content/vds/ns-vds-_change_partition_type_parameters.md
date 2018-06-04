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
 

 

