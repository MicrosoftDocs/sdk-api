---
UID: NS:vds._VDS_PARTITION_INFO_MBR
title: VDS_PARTITION_INFO_MBR (vds.h)
description: Defines the details of a master boot record (MBR) partition.
helpviewer_keywords: ["VDS_PARTITION_INFO_MBR","VDS_PARTITION_INFO_MBR structure [VDS]","base.vds_partition_info_mbr","vds/_VDS_PARTITION_INFO_MBR"]
old-location: base\vds_partition_info_mbr.htm
tech.root: base
ms.assetid: d14a852f-8a78-4631-a288-476701321ac2
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_INFO_MBR, VDS_PARTITION_INFO_MBR structure [VDS], base.vds_partition_info_mbr, vds/_VDS_PARTITION_INFO_MBR
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
req.typenames: VDS_PARTITION_INFO_MBR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PARTITION_INFO_MBR
 - vds/_VDS_PARTITION_INFO_MBR
 - VDS_PARTITION_INFO_MBR
 - vds/VDS_PARTITION_INFO_MBR
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
 - VDS_PARTITION_INFO_MBR
---

# VDS_PARTITION_INFO_MBR structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of a master boot record (MBR) partition.

## -struct-fields

### -field partitionType

Byte value indicating the partition type.

### -field bootIndicator

If true, the partition is active and can be booted; otherwise, the partition cannot be used to boot the computer.

### -field recognizedPartition

If true, the operating system recognizes the partition style; otherwise, the partition style is unknown.

### -field hiddenSectors

Reserved sectors.

## -remarks

This structure is used in the <b>Mbr</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a> structure.

For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>