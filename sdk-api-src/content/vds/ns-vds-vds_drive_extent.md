---
UID: NS:vds._VDS_DRIVE_EXTENT
title: VDS_DRIVE_EXTENT
author: windows-sdk-content
description: Defines the properties of a drive extent.
old-location: base\vds_drive_extent.htm
tech.root: VDS
ms.assetid: c155d925-e86f-4bec-9032-dae2221172a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_DRIVE_EXTENT, VDS_DRIVE_EXTENT, VDS_DRIVE_EXTENT structure [VDS], base.vds_drive_extent, vds/_VDS_DRIVE_EXTENT, vdshwprv/_VDS_DRIVE_EXTENT"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: VDS_DRIVE_EXTENT, *PVDS_DRIVE_EXTENT
req.redist: 
---

# VDS_DRIVE_EXTENT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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



The <a href="https://msdn.microsoft.com/8ee3e085-ce69-457e-b652-bb9c45b7fdd8">IVdsDrive::QueryExtents</a> 
    method returns this structure to report the properties of a drive extent. It is also returned by the 
    <a href="https://msdn.microsoft.com/e9ed5bdd-c696-47cc-84c8-266b230f7970">IVdsLunPlex::QueryExtents</a> method to report 
    the details of a drive extent that is allocated to a plex.

A disk extent is a contiguous set of blocks on a single disk or LUN handled by a software provider. A drive 
    extent is not required to be a contiguous set of blocks.




## -see-also




<a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">Drive Object</a>



<a href="https://msdn.microsoft.com/8ee3e085-ce69-457e-b652-bb9c45b7fdd8">IVdsDrive::QueryExtents</a>



<a href="https://msdn.microsoft.com/e9ed5bdd-c696-47cc-84c8-266b230f7970">IVdsLunPlex::QueryExtents</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

