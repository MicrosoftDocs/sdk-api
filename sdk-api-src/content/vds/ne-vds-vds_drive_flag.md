---
UID: NE:vds._VDS_DRIVE_FLAG
title: VDS_DRIVE_FLAG (vds.h)
author: windows-sdk-content
description: Defines the set of valid flags for a drive object.
old-location: base\vds_drive_flag.htm
tech.root: VDS
ms.assetid: 50ddb9d1-32c9-4fee-bb88-498380a34c85
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_DRIVE_FLAG, VDS_DRF_ASSIGNED, VDS_DRF_HOTSPARE, VDS_DRF_HOTSPARE_IN_USE, VDS_DRF_HOTSPARE_STANDBY, VDS_DRF_UNASSIGNED, VDS_DRIVE_FLAG, VDS_DRIVE_FLAG enumeration [VDS], base.vds_drive_flag, vds/VDS_DRF_ASSIGNED, vds/VDS_DRF_HOTSPARE, vds/VDS_DRF_HOTSPARE_IN_USE, vds/VDS_DRF_HOTSPARE_STANDBY, vds/VDS_DRF_UNASSIGNED, vds/VDS_DRIVE_FLAG, vdshwprv/VDS_DRF_ASSIGNED, vdshwprv/VDS_DRF_HOTSPARE, vdshwprv/VDS_DRF_HOTSPARE_IN_USE, vdshwprv/VDS_DRF_HOTSPARE_STANDBY, vdshwprv/VDS_DRF_UNASSIGNED, vdshwprv/VDS_DRIVE_FLAG"
ms.topic: enum
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
 - VDS_DRIVE_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_DRIVE_FLAG, *PVDS_DRIVE_FLAG
req.redist: 
---

# VDS_DRIVE_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a <a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">drive object</a>.


## -enum-fields




### -field VDS_DRF_HOTSPARE

The drive is reserved for use only as a hot spare.


### -field VDS_DRF_ASSIGNED

The drive is assigned to a RAID group or <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_DRF_UNASSIGNED

The drive is not assigned to a RAID group or storage pool.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_DRF_HOTSPARE_IN_USE

The drive is in use as a hot spare.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_DRF_HOTSPARE_STANDBY

The drive is on standby as a hot spare.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the  <a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>structure.

This enumeration provides the values for the <i>ulFlags</i> member of the  <a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DRIVE_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DRIVE_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>



<a href="https://msdn.microsoft.com/af932865-abb3-4dee-a7dc-3aa06fd167f6">VDS_DRIVE_PROP2</a>
 

 

