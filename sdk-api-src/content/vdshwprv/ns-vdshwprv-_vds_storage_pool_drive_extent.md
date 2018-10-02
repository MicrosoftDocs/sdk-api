---
UID: NS:vdshwprv._VDS_STORAGE_POOL_DRIVE_EXTENT
title: "_VDS_STORAGE_POOL_DRIVE_EXTENT"
author: windows-sdk-content
description: Defines a drive extent that could be used by a storage pool.
old-location: base\vds_storage_pool_drive_extent.htm
tech.root: VDS
ms.assetid: e8b4a4c7-04d5-48b5-ba44-bb99cbf9fc60
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVDS_STORAGE_POOL_DRIVE_EXTENT, PVDS_STORAGE_POOL_DRIVE_EXTENT, PVDS_STORAGE_POOL_DRIVE_EXTENT structure pointer, VDS_STORAGE_POOL_DRIVE_EXTENT, VDS_STORAGE_POOL_DRIVE_EXTENT structure, _VDS_STORAGE_POOL_DRIVE_EXTENT, base.vds_storage_pool_drive_extent, vds/PVDS_STORAGE_POOL_DRIVE_EXTENT, vds/VDS_STORAGE_POOL_DRIVE_EXTENT, vdshwprv/PVDS_STORAGE_POOL_DRIVE_EXTENT, vdshwprv/VDS_STORAGE_POOL_DRIVE_EXTENT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdshwprv.h
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
product: Windows
targetos: Windows
req.typenames: VDS_STORAGE_POOL_DRIVE_EXTENT, *PVDS_STORAGE_POOL_DRIVE_EXTENT
req.redist: 
---

# _VDS_STORAGE_POOL_DRIVE_EXTENT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a drive extent that could be used by a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.


## -struct-fields




### -field id

A <a href="https://msdn.microsoft.com/f17e8c7e-e3cb-49ca-9060-2299dda55770">VDS_OBJECT_ID</a> value that identifies the <a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">drive object</a>.


### -field ullSize

Size, in bytes, of the drive extent.


### -field bUsed

<b>TRUE</b> if the drive extent is currently being used by the storage pool, <b>FALSE</b> otherwise.


## -see-also




<a href="https://msdn.microsoft.com/91bae6e6-3718-4d82-ab8c-e489b9a105fe">IVdsStoragePool::QueryDriveExtents</a>



<a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>
 

 

