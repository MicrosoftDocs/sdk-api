---
UID: NS:vdshwprv._VDS_DRIVE_EXTENT
title: VDS_DRIVE_EXTENT (vdshwprv.h)
description: The VDS_DRIVE_EXTENT structure (vdshwprv.h) defines the properties of a drive extent.
helpviewer_keywords: ["*PVDS_DRIVE_EXTENT","VDS_DRIVE_EXTENT","VDS_DRIVE_EXTENT structure [VDS]","base.vds_drive_extent","vds/_VDS_DRIVE_EXTENT","vdshwprv/_VDS_DRIVE_EXTENT"]
old-location: base\vds_drive_extent.htm
tech.root: base
ms.assetid: c155d925-e86f-4bec-9032-dae2221172a7
ms.date: 08/08/2022
ms.keywords: '*PVDS_DRIVE_EXTENT, VDS_DRIVE_EXTENT, VDS_DRIVE_EXTENT structure [VDS], base.vds_drive_extent, vds/_VDS_DRIVE_EXTENT, vdshwprv/_VDS_DRIVE_EXTENT'
req.header: vdshwprv.h
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
req.typenames: VDS_DRIVE_EXTENT, *PVDS_DRIVE_EXTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_EXTENT
 - vdshwprv/_VDS_DRIVE_EXTENT
 - PVDS_DRIVE_EXTENT
 - vdshwprv/PVDS_DRIVE_EXTENT
 - VDS_DRIVE_EXTENT
 - vdshwprv/VDS_DRIVE_EXTENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_DRIVE_EXTENT
---

# VDS_DRIVE_EXTENT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a drive extent.

## -struct-fields

### -field id

The <b>VDS_OBJECT_ID</b> of the drive.

### -field LunId

The <b>VDS_OBJECT_ID</b> of the LUN that is associated with the drive extent.

### -field ullSize

The size of the extent, in bytes.

### -field bUsed

If <b>TRUE</b>, the extent is allocated to a LUN plex. If <b>FALSE</b>, the extent is unallocated.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-queryextents">IVdsDrive::QueryExtents</a> 
    method returns this structure to report the properties of a drive extent. It is also returned by the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a> method to report 
    the details of a drive extent that is allocated to a plex.

A disk extent is a contiguous set of blocks on a single disk or LUN handled by a software provider. A drive 
    extent is not required to be a contiguous set of blocks.

## -see-also

<a href="/windows/desktop/VDS/drive-object">Drive Object</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-queryextents">IVdsDrive::QueryExtents</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>
