---
UID: NS:vds._VDS_STORAGE_POOL_DRIVE_EXTENT
title: VDS_STORAGE_POOL_DRIVE_EXTENT (vds.h)
description: Defines a drive extent that could be used by a storage pool.helpviewer_keywords: ["*PVDS_STORAGE_POOL_DRIVE_EXTENT","PVDS_STORAGE_POOL_DRIVE_EXTENT","PVDS_STORAGE_POOL_DRIVE_EXTENT structure pointer","VDS_STORAGE_POOL_DRIVE_EXTENT","VDS_STORAGE_POOL_DRIVE_EXTENT structure","base.vds_storage_pool_drive_extent","vds/PVDS_STORAGE_POOL_DRIVE_EXTENT","vds/VDS_STORAGE_POOL_DRIVE_EXTENT","vdshwprv/PVDS_STORAGE_POOL_DRIVE_EXTENT","vdshwprv/VDS_STORAGE_POOL_DRIVE_EXTENT"]
old-location: base\vds_storage_pool_drive_extent.htm
tech.root: VDS
ms.assetid: e8b4a4c7-04d5-48b5-ba44-bb99cbf9fc60
ms.date: 12/05/2018
ms.keywords: '*PVDS_STORAGE_POOL_DRIVE_EXTENT, PVDS_STORAGE_POOL_DRIVE_EXTENT, PVDS_STORAGE_POOL_DRIVE_EXTENT structure pointer, VDS_STORAGE_POOL_DRIVE_EXTENT, VDS_STORAGE_POOL_DRIVE_EXTENT structure, base.vds_storage_pool_drive_extent, vds/PVDS_STORAGE_POOL_DRIVE_EXTENT, vds/VDS_STORAGE_POOL_DRIVE_EXTENT, vdshwprv/PVDS_STORAGE_POOL_DRIVE_EXTENT, vdshwprv/VDS_STORAGE_POOL_DRIVE_EXTENT'
f1_keywords:
- vds/VDS_STORAGE_POOL_DRIVE_EXTENT
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_STORAGE_POOL_DRIVE_EXTENT
targetos: Windows
req.typenames: VDS_STORAGE_POOL_DRIVE_EXTENT, *PVDS_STORAGE_POOL_DRIVE_EXTENT
req.redist: 
ms.custom: 19H1
---

# VDS_STORAGE_POOL_DRIVE_EXTENT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a drive extent that could be used by a <a href="https://docs.microsoft.com/windows/desktop/VDS/storage-pool-object">storage pool</a>.


## -struct-fields




### -field id

A <a href="https://docs.microsoft.com/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> value that identifies the <a href="https://docs.microsoft.com/windows/desktop/VDS/drive-object">drive object</a>.


### -field ullSize

Size, in bytes, of the drive extent.


### -field bUsed

<b>TRUE</b> if the drive extent is currently being used by the storage pool, <b>FALSE</b> otherwise.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-querydriveextents">IVdsStoragePool::QueryDriveExtents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a>
 

 

