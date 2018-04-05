---
UID: NS:vds._VDS_DISK_FREE_EXTENT
title: "_VDS_DISK_FREE_EXTENT"
author: windows-driver-content
description: Describes a free extent on a disk.
old-location: base\vds_disk_free_extent.htm
old-project: VDS
ms.assetid: 94beebd5-bfd6-410f-94b9-51c8e3609bf6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PVDS_DISK_FREE_EXTENT, PVDS_DISK_FREE_EXTENT, PVDS_DISK_FREE_EXTENT structure pointer, VDS_DISK_FREE_EXTENT, VDS_DISK_FREE_EXTENT structure, _VDS_DISK_FREE_EXTENT, base.vds_disk_free_extent, vds/PVDS_DISK_FREE_EXTENT, vds/VDS_DISK_FREE_EXTENT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: VDS_DISK_FREE_EXTENT, *PVDS_DISK_FREE_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_DISK_FREE_EXTENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_DISK_FREE_EXTENT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Describes a free extent on a disk.


## -struct-fields




### -field diskId

The <a href="https://msdn.microsoft.com/f17e8c7e-e3cb-49ca-9060-2299dda55770">VDS_OBJECT_ID</a> of the disk.


### -field ullOffset

The disk offset, in bytes, of the free extent.


### -field ullSize

The size, in bytes, of the free extent.


## -see-also




<a href="https://msdn.microsoft.com/0ca2ebb6-1394-48a2-972b-bdf43bf58ced">IVdsDisk3::QueryFreeExtents</a>
 

 

