---
UID: NE:vds._VDS_PARTITION_STYLE
title: "_VDS_PARTITION_STYLE"
author: windows-sdk-content
description: Defines the set of partition style values.
old-location: base\vds_partition_style.htm
old-project: vds
ms.assetid: 31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_PARTITION_STYLE, VDS_PARTITION_STYLE enumeration [VDS], VDS_PST_GPT, VDS_PST_MBR, VDS_PST_UNKNOWN, _VDS_PARTITION_STYLE, base.vds_partition_style, vds/VDS_PARTITION_STYLE, vds/VDS_PST_GPT, vds/VDS_PST_MBR, vds/VDS_PST_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.redist: 
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
req.typenames: VDS_PARTITION_STYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_PARTITION_STYLE
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_PARTITION_STYLE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of partition style values.


## -enum-fields




### -field VDS_PST_UNKNOWN

An uninitialized disk. New disks or newly cleaned disks have this partitioning type.


### -field VDS_PST_MBR

The style is master boot record (MBR). If the value is <b>VDS_PST_MBR</b>, a DWORD signature  identifies the disk. The identifier is unique on a single computer, but not unique across multiple computers. See the <a href="https://msdn.microsoft.com/d14a852f-8a78-4631-a288-476701321ac2">VDS_PARTITION_INFO_MBR</a> structure.


### -field VDS_PST_GPT

The style is GUID partition table (GPT). If the value is <b>VDS_PST_GPT</b>, the disk has a GUID identifier. The GUID is guaranteed statistically to be unique across different computers. See the <a href="https://msdn.microsoft.com/5c484155-df73-4007-a137-998c7f1c5a7c">VDS_PARTITION_INFO_GPT</a> structure.


## -remarks



The <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and
        <a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a>structures include a <b>VDS_PARTITION_STYLE</b> value as a member. Additionally, the  <a href="https://msdn.microsoft.com/38c129cd-8e60-4e4a-b22b-26c69c68fe89">IVdsDisk::ConvertStyle</a>and <a href="https://msdn.microsoft.com/e64e3891-74c6-4014-9909-24f75f69e06d">IVdsPack::AddDisk</a>methods pass a <b>VDS_PARTITION_STYLE</b> value  as an argument to indicate the partition style on a disk.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PARTITION_STYLE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PARTITION_STYLE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/38c129cd-8e60-4e4a-b22b-26c69c68fe89">IVdsDisk::ConvertStyle</a>



<a href="https://msdn.microsoft.com/e64e3891-74c6-4014-9909-24f75f69e06d">IVdsPack::AddDisk</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a>
 

 

