---
UID: NS:vds._VDS_DISK_FREE_EXTENT
title: VDS_DISK_FREE_EXTENT (vds.h)
description: Describes a free extent on a disk.
helpviewer_keywords: ["*PVDS_DISK_FREE_EXTENT","PVDS_DISK_FREE_EXTENT","PVDS_DISK_FREE_EXTENT structure pointer","VDS_DISK_FREE_EXTENT","VDS_DISK_FREE_EXTENT structure","base.vds_disk_free_extent","vds/PVDS_DISK_FREE_EXTENT","vds/VDS_DISK_FREE_EXTENT"]
old-location: base\vds_disk_free_extent.htm
tech.root: base
ms.assetid: 94beebd5-bfd6-410f-94b9-51c8e3609bf6
ms.date: 12/05/2018
ms.keywords: '*PVDS_DISK_FREE_EXTENT, PVDS_DISK_FREE_EXTENT, PVDS_DISK_FREE_EXTENT structure pointer, VDS_DISK_FREE_EXTENT, VDS_DISK_FREE_EXTENT structure, base.vds_disk_free_extent, vds/PVDS_DISK_FREE_EXTENT, vds/VDS_DISK_FREE_EXTENT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_DISK_FREE_EXTENT, *PVDS_DISK_FREE_EXTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_FREE_EXTENT
 - vds/_VDS_DISK_FREE_EXTENT
 - PVDS_DISK_FREE_EXTENT
 - vds/PVDS_DISK_FREE_EXTENT
 - VDS_DISK_FREE_EXTENT
 - vds/VDS_DISK_FREE_EXTENT
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
 - VDS_DISK_FREE_EXTENT
---

# VDS_DISK_FREE_EXTENT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Describes a free extent on a disk.

## -struct-fields

### -field diskId

The <a href="/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> of the disk.

### -field ullOffset

The disk offset, in bytes, of the free extent.

### -field ullSize

The size, in bytes, of the free extent.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-queryfreeextents">IVdsDisk3::QueryFreeExtents</a>