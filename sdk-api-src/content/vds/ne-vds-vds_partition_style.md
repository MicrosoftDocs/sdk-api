---
UID: NE:vds._VDS_PARTITION_STYLE
title: VDS_PARTITION_STYLE (vds.h)
author: windows-sdk-content
description: Defines the set of partition style values.
old-location: base\vds_partition_style.htm
tech.root: VDS
ms.assetid: 31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_STYLE, VDS_PARTITION_STYLE enumeration [VDS], VDS_PST_GPT, VDS_PST_MBR, VDS_PST_UNKNOWN, base.vds_partition_style, vds/VDS_PARTITION_STYLE, vds/VDS_PST_GPT, vds/VDS_PST_MBR, vds/VDS_PST_UNKNOWN
ms.topic: enum
f1_keywords: ["vds/VDS_PARTITION_STYLE"]
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
 - VDS_PARTITION_STYLE
product: Windows
targetos: Windows
req.typenames: VDS_PARTITION_STYLE
req.redist: 
ms.custom: 19H1
---

# VDS_PARTITION_STYLE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of partition style values.


## -enum-fields




### -field VDS_PST_UNKNOWN

An uninitialized disk. New disks or newly cleaned disks have this partitioning type.


### -field VDS_PST_MBR

The style is master boot record (MBR). If the value is <b>VDS_PST_MBR</b>, a DWORD signature  identifies the disk. The identifier is unique on a single computer, but not unique across multiple computers. See the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a> structure.


### -field VDS_PST_GPT

The style is GUID partition table (GPT). If the value is <b>VDS_PST_GPT</b>, the disk has a GUID identifier. The GUID is guaranteed statistically to be unique across different computers. See the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a> structure.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_disk_prop">VDS_DISK_PROP</a> and
        <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_prop">VDS_PARTITION_PROP</a>structures include a <b>VDS_PARTITION_STYLE</b> value as a member. Additionally, the  <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-convertstyle">IVdsDisk::ConvertStyle</a>and <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-adddisk">IVdsPack::AddDisk</a>methods pass a <b>VDS_PARTITION_STYLE</b> value  as an argument to indicate the partition style on a disk.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PARTITION_STYLE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PARTITION_STYLE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-convertstyle">IVdsDisk::ConvertStyle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-adddisk">IVdsPack::AddDisk</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_disk_prop">VDS_DISK_PROP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_partition_prop">VDS_PARTITION_PROP</a>
 

 

