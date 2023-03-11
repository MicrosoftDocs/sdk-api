---
UID: NS:vds._VDS_DISK_EXTENT
title: VDS_DISK_EXTENT (vds.h)
description: Defines the properties of a disk extent.
helpviewer_keywords: ["*PVDS_DISK_EXTENT","PVDS_DISK_EXTENT","PVDS_DISK_EXTENT structure pointer [VDS]","VDS_DISK_EXTENT","VDS_DISK_EXTENT structure [VDS]","base.vds_disk_extent","vds/PVDS_DISK_EXTENT","vds/_VDS_DISK_EXTENT"]
old-location: base\vds_disk_extent.htm
tech.root: base
ms.assetid: 79fa7b8a-9d24-49ab-8e5d-1471b023c459
ms.date: 12/05/2018
ms.keywords: '*PVDS_DISK_EXTENT, PVDS_DISK_EXTENT, PVDS_DISK_EXTENT structure pointer [VDS], VDS_DISK_EXTENT, VDS_DISK_EXTENT structure [VDS], base.vds_disk_extent, vds/PVDS_DISK_EXTENT, vds/_VDS_DISK_EXTENT'
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
req.typenames: VDS_DISK_EXTENT, *PVDS_DISK_EXTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_EXTENT
 - vds/_VDS_DISK_EXTENT
 - PVDS_DISK_EXTENT
 - vds/PVDS_DISK_EXTENT
 - VDS_DISK_EXTENT
 - vds/VDS_DISK_EXTENT
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
 - VDS_DISK_EXTENT
---

# VDS_DISK_EXTENT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of 
   a disk extent.

## -struct-fields

### -field diskId

The GUID of the disk.

### -field type

A <a href="/windows/desktop/api/vds/ne-vds-vds_disk_extent_type">VDS_DISK_EXTENT_TYPE</a> enumeration value that specifies the type of the disk extent.

### -field ullOffset

The disk offset, in bytes.

### -field ullSize

The size of the extent, in bytes.

### -field volumeId

The GUID of the volume to which the extent belongs.

### -field plexId

If the extent is from a volume, this member is the GUID of the plex to which the extent belongs.

### -field memberIdx

If the extent is from a volume plex, this member is the zero-based index of the plex member to which the extent belongs.

## -remarks

The <i>volumeId</i>, <i>plexId</i>, and 
    <i>memberIdx</i> members apply to data and ESP partitions only. If the extent lacks a volume 
    association, the GUIDs for <i>volumeId</i> and <i>plexId</i> are GUID_NULL, 
    and <i>memberIdx</i> is zero. The <i>memberIdx</i> member is always zero 
    unless the volume is striped or striped with parity (RAID-5). An extent can also be unallocated or free.
   

The <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-queryextents">IVdsDisk::QueryExtents</a> method returns this 
    structure to report the property details of a disk extent. Likewise, the 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-queryextents">IVdsVolumePlex::QueryExtents</a> method 
    returns it to report the details of the disk extents allocated to a plex.

A disk extent is a contiguous set of blocks on a single disk or LUN handled by a software provider. A drive 
    extent is not required to be a contiguous set of blocks.

## -see-also

<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-queryextents">IVdsDisk::QueryExtents</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-queryextents">IVdsVolumePlex::QueryExtents</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_extent_type">VDS_DISK_EXTENT_TYPE</a>