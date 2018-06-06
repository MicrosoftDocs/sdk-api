---
UID: NE:vds._VDS_FORMAT_OPTION_FLAGS
title: "_VDS_FORMAT_OPTION_FLAGS"
author: windows-sdk-content
description: Defines the set of valid formatting options for the IVdsDiskPartitionMF2::FormatPartitionEx2 method.
old-location: base\vds_format_option_flags.htm
old-project: VDS
ms.assetid: 75c92a9a-36c9-4c8d-90f2-a2b88cd8a7b5
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_FORMAT_OPTION_FLAGS, VDS_FORMAT_OPTION_FLAGS enumeration, VDS_FSOF_COMPRESSION, VDS_FSOF_DUPLICATE_METADATA, VDS_FSOF_FORCE, VDS_FSOF_NONE, VDS_FSOF_QUICK, _VDS_FORMAT_OPTION_FLAGS, base.vds_format_option_flags, vds/VDS_FORMAT_OPTION_FLAGS, vds/VDS_FSOF_COMPRESSION, vds/VDS_FSOF_DUPLICATE_METADATA, vds/VDS_FSOF_FORCE, vds/VDS_FSOF_NONE, vds/VDS_FSOF_QUICK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_FORMAT_OPTION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FORMAT_OPTION_FLAGS
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
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
 

 

