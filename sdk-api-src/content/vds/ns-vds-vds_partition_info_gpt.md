---
UID: NS:vds._VDS_PARTITION_INFO_GPT
title: VDS_PARTITION_INFO_GPT (vds.h)
description: Defines details of a GUID partition table (GPT) partition.
helpviewer_keywords: ["VDS_PARTITION_INFO_GPT","VDS_PARTITION_INFO_GPT structure [VDS]","base.vds_partition_info_gpt","vds/_VDS_PARTITION_INFO_GPT"]
old-location: base\vds_partition_info_gpt.htm
tech.root: base
ms.assetid: 5c484155-df73-4007-a137-998c7f1c5a7c
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_INFO_GPT, VDS_PARTITION_INFO_GPT structure [VDS], base.vds_partition_info_gpt, vds/_VDS_PARTITION_INFO_GPT
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
req.typenames: VDS_PARTITION_INFO_GPT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PARTITION_INFO_GPT
 - vds/_VDS_PARTITION_INFO_GPT
 - VDS_PARTITION_INFO_GPT
 - vds/VDS_PARTITION_INFO_GPT
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
 - VDS_PARTITION_INFO_GPT
---

# VDS_PARTITION_INFO_GPT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines details of a GUID partition table (GPT) partition.

## -struct-fields

### -field partitionType

GUID for the partition type.

### -field partitionId

GUID for the partition.

### -field attributes

Attributes of the partition.

### -field name

Name of the partition.

## -remarks

This structure is used in the <b>Gpt</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a> structure.

 A GPT table is sector-aligned.

For information about partition types and attributes, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a>