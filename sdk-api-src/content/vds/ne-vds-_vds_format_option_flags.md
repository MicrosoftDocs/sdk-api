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

# _VDS_FORMAT_OPTION_FLAGS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid formatting options for the <a href="https://msdn.microsoft.com/2a37d3c7-5c03-4b19-9d82-c3b16bf980e1">IVdsDiskPartitionMF2::FormatPartitionEx2</a> method.


## -enum-fields




### -field VDS_FSOF_NONE

No options are specified.


### -field VDS_FSOF_FORCE

The format operation should be forced, even if the partition is in use.


### -field VDS_FSOF_QUICK

Perform a quick format operation. A quick format does not verify each sector on the volume.


### -field VDS_FSOF_COMPRESSION

Enable compression on the newly formatted file system volume. Compression is a feature of the NTFS file system; it cannot be set for other file systems such as FAT or FAT32.


### -field VDS_FSOF_DUPLICATE_METADATA

Forces duplication of metadata for UDF 2.5 and above.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FORMAT_OPTION_FLAGS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FORMAT_OPTION_FLAGS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a37d3c7-5c03-4b19-9d82-c3b16bf980e1">IVdsDiskPartitionMF2::FormatPartitionEx2</a>
 

 

