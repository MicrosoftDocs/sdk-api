---
UID: NE:vds._VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
title: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG (vds.h)
author: windows-sdk-content
description: Defines the properties of file systems that are supported for formatting volumes.
old-location: base\vds_file_system_format_support_flag.htm
tech.root: VDS
ms.assetid: 78d60240-44dc-48b8-b2a6-5babbd79085f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG, VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG enumeration, VDS_FSS_DEFAULT, VDS_FSS_PREVIOUS_REVISION, VDS_FSS_RECOMMENDED, base.vds_file_system_format_support_flag, vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG, vds/VDS_FSS_DEFAULT, vds/VDS_FSS_PREVIOUS_REVISION, vds/VDS_FSS_RECOMMENDED
ms.topic: enum
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
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
req.redist: 
---

# VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of file systems that are supported for formatting volumes. These values are used in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/0a0863d3-a97f-4be5-bba4-15d6bbbf03a5">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a> structure.


## -enum-fields




### -field VDS_FSS_DEFAULT

The file system is the default file system to be used for formatting the volume.


### -field VDS_FSS_PREVIOUS_REVISION

The revision of the file system is not the latest revision supported for formatting the volume.


### -field VDS_FSS_RECOMMENDED

The file system is the recommended file system to be used for formatting the volume.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a37d3c7-5c03-4b19-9d82-c3b16bf980e1">IVdsDiskPartitionMF2::FormatPartitionEx2</a>



<a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a>



<a href="https://msdn.microsoft.com/0a0863d3-a97f-4be5-bba4-15d6bbbf03a5">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a>
 

 

