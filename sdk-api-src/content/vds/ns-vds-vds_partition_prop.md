---
UID: NS:vds._VDS_PARTITION_PROP
title: VDS_PARTITION_PROP (vds.h)
description: Defines the properties of a partition.
helpviewer_keywords: ["VDS_PARTITION_PROP","VDS_PARTITION_PROP structure [VDS]","base.vds_partition_prop","vds/_VDS_PARTITION_PROP"]
old-location: base\vds_partition_prop.htm
tech.root: base
ms.assetid: f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_PROP, VDS_PARTITION_PROP structure [VDS], base.vds_partition_prop, vds/_VDS_PARTITION_PROP
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
targetos: Windows
req.typenames: VDS_PARTITION_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PARTITION_PROP
 - vds/_VDS_PARTITION_PROP
 - VDS_PARTITION_PROP
 - vds/VDS_PARTITION_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_PARTITION_PROP
---

# VDS_PARTITION_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a partition.

## -struct-fields

### -field PartitionStyle

The styles enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>. 
      The style is either master boot record (VDS_PST_MBR) or GUID partition table (VDS_PST_GPT). This member is the
      discriminant for the union.

### -field ulFlags

The partition flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_partition_flag">VDS_PARTITION_FLAG</a>.

### -field ulPartitionNumber

The number assigned to the partition.

### -field ullOffset

The partition offset.

### -field ullSize

The size of the partition in bytes.

### -field Mbr

If <b>PartitionStyle</b> is <b>VDS_PST_MBR</b>, MBR-specific partition 
       details. For more information see 
       <a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a>.

### -field Gpt

If <b>PartitionStyle</b> is <b>VDS_PST_GPT</b>, GPT-specific partition 
       details. For more information see 
       <a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getpartitionproperties">IVdsAdvancedDisk::GetPartitionProperties</a> 
    and <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-querypartitions">IVdsAdvancedDisk::QueryPartitions</a> 
    methods return this structure to report the property details of a partition.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getpartitionproperties">IVdsAdvancedDisk::GetPartitionProperties</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-querypartitions">IVdsAdvancedDisk::QueryPartitions</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_flag">VDS_PARTITION_FLAG</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>