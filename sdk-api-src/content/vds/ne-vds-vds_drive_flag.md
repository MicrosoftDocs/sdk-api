---
UID: NE:vds._VDS_DRIVE_FLAG
title: VDS_DRIVE_FLAG (vds.h)
description: Defines the set of valid flags for a drive object.
helpviewer_keywords: ["*PVDS_DRIVE_FLAG","VDS_DRF_ASSIGNED","VDS_DRF_HOTSPARE","VDS_DRF_HOTSPARE_IN_USE","VDS_DRF_HOTSPARE_STANDBY","VDS_DRF_UNASSIGNED","VDS_DRIVE_FLAG","VDS_DRIVE_FLAG enumeration [VDS]","base.vds_drive_flag","vds/VDS_DRF_ASSIGNED","vds/VDS_DRF_HOTSPARE","vds/VDS_DRF_HOTSPARE_IN_USE","vds/VDS_DRF_HOTSPARE_STANDBY","vds/VDS_DRF_UNASSIGNED","vds/VDS_DRIVE_FLAG","vdshwprv/VDS_DRF_ASSIGNED","vdshwprv/VDS_DRF_HOTSPARE","vdshwprv/VDS_DRF_HOTSPARE_IN_USE","vdshwprv/VDS_DRF_HOTSPARE_STANDBY","vdshwprv/VDS_DRF_UNASSIGNED","vdshwprv/VDS_DRIVE_FLAG"]
old-location: base\vds_drive_flag.htm
tech.root: base
ms.assetid: 50ddb9d1-32c9-4fee-bb88-498380a34c85
ms.date: 12/05/2018
ms.keywords: '*PVDS_DRIVE_FLAG, VDS_DRF_ASSIGNED, VDS_DRF_HOTSPARE, VDS_DRF_HOTSPARE_IN_USE, VDS_DRF_HOTSPARE_STANDBY, VDS_DRF_UNASSIGNED, VDS_DRIVE_FLAG, VDS_DRIVE_FLAG enumeration [VDS], base.vds_drive_flag, vds/VDS_DRF_ASSIGNED, vds/VDS_DRF_HOTSPARE, vds/VDS_DRF_HOTSPARE_IN_USE, vds/VDS_DRF_HOTSPARE_STANDBY, vds/VDS_DRF_UNASSIGNED, vds/VDS_DRIVE_FLAG, vdshwprv/VDS_DRF_ASSIGNED, vdshwprv/VDS_DRF_HOTSPARE, vdshwprv/VDS_DRF_HOTSPARE_IN_USE, vdshwprv/VDS_DRF_HOTSPARE_STANDBY, vdshwprv/VDS_DRF_UNASSIGNED, vdshwprv/VDS_DRIVE_FLAG'
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
req.typenames: VDS_DRIVE_FLAG, *PVDS_DRIVE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_FLAG
 - vds/_VDS_DRIVE_FLAG
 - PVDS_DRIVE_FLAG
 - vds/PVDS_DRIVE_FLAG
 - VDS_DRIVE_FLAG
 - vds/VDS_DRIVE_FLAG
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
 - VDS_DRIVE_FLAG
---

# VDS_DRIVE_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for a <a href="/windows/desktop/VDS/drive-object">drive object</a>.

## -enum-fields

### -field VDS_DRF_HOTSPARE:0x1

The drive is reserved for use only as a hot spare.

### -field VDS_DRF_ASSIGNED:0x2

The drive is assigned to a RAID group or <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_DRF_UNASSIGNED:0x4

The drive is not assigned to a RAID group or storage pool.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_DRF_HOTSPARE_IN_USE:0x8

The drive is in use as a hot spare.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_DRF_HOTSPARE_STANDBY:0x10

The drive is on standby as a hot spare.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the  <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a> structure.

This enumeration provides the values for the <i>ulFlags</i> member of the  <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DRIVE_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DRIVE_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop2">VDS_DRIVE_PROP2</a>
