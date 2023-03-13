---
UID: NS:vds._CHANGE_PARTITION_TYPE_PARAMETERS
title: CHANGE_PARTITION_TYPE_PARAMETERS (vds.h)
description: Describes parameters to be used when changing a partition's type.
helpviewer_keywords: ["CHANGE_PARTITION_TYPE_PARAMETERS","CHANGE_PARTITION_TYPE_PARAMETERS structure","PCHANGE_PARTITION_TYPE_PARAMETERS","PCHANGE_PARTITION_TYPE_PARAMETERS structure pointer","base.change_partition_type_parameters","vds/CHANGE_PARTITION_TYPE_PARAMETERS","vds/PCHANGE_PARTITION_TYPE_PARAMETERS"]
old-location: base\change_partition_type_parameters.htm
tech.root: base
ms.assetid: bd51c2a6-ab26-4a2f-89f4-431d05f3dd81
ms.date: 12/05/2018
ms.keywords: CHANGE_PARTITION_TYPE_PARAMETERS, CHANGE_PARTITION_TYPE_PARAMETERS structure, PCHANGE_PARTITION_TYPE_PARAMETERS, PCHANGE_PARTITION_TYPE_PARAMETERS structure pointer, base.change_partition_type_parameters, vds/CHANGE_PARTITION_TYPE_PARAMETERS, vds/PCHANGE_PARTITION_TYPE_PARAMETERS
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
targetos: Windows
req.typenames: CHANGE_PARTITION_TYPE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CHANGE_PARTITION_TYPE_PARAMETERS
 - vds/_CHANGE_PARTITION_TYPE_PARAMETERS
 - CHANGE_PARTITION_TYPE_PARAMETERS
 - vds/CHANGE_PARTITION_TYPE_PARAMETERS
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
 - CHANGE_PARTITION_TYPE_PARAMETERS
---

# CHANGE_PARTITION_TYPE_PARAMETERS structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Describes parameters to be used when changing a partition's type.

## -struct-fields

### -field style

A value from the <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a> enumeration that describes the disk's partition style.

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

For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk2-changepartitiontype">IVdsAdvancedDisk2::ChangePartitionType</a>