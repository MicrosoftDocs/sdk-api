---
UID: NE:vds._VDS_DISK_STATUS
title: VDS_DISK_STATUS (vds.h)
description: Defines the set of object status values for a disk.
helpviewer_keywords: ["VDS_DISK_STATUS","VDS_DISK_STATUS enumeration [VDS]","VDS_DS_FAILED","VDS_DS_MISSING","VDS_DS_NOT_READY","VDS_DS_NO_MEDIA","VDS_DS_OFFLINE","VDS_DS_ONLINE","VDS_DS_UNKNOWN","base.vds_disk_status","vds/VDS_DISK_STATUS","vds/VDS_DS_FAILED","vds/VDS_DS_MISSING","vds/VDS_DS_NOT_READY","vds/VDS_DS_NO_MEDIA","vds/VDS_DS_OFFLINE","vds/VDS_DS_ONLINE","vds/VDS_DS_UNKNOWN"]
old-location: base\vds_disk_status.htm
tech.root: base
ms.assetid: 7691347d-49a6-4078-9c6c-af59a48af692
ms.date: 12/05/2018
ms.keywords: VDS_DISK_STATUS, VDS_DISK_STATUS enumeration [VDS], VDS_DS_FAILED, VDS_DS_MISSING, VDS_DS_NOT_READY, VDS_DS_NO_MEDIA, VDS_DS_OFFLINE, VDS_DS_ONLINE, VDS_DS_UNKNOWN, base.vds_disk_status, vds/VDS_DISK_STATUS, vds/VDS_DS_FAILED, vds/VDS_DS_MISSING, vds/VDS_DS_NOT_READY, vds/VDS_DS_NO_MEDIA, vds/VDS_DS_OFFLINE, vds/VDS_DS_ONLINE, vds/VDS_DS_UNKNOWN
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
req.typenames: VDS_DISK_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_STATUS
 - vds/_VDS_DISK_STATUS
 - VDS_DISK_STATUS
 - vds/VDS_DISK_STATUS
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
 - VDS_DISK_STATUS
---

# VDS_DISK_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a disk.

## -enum-fields

### -field VDS_DS_UNKNOWN:0

The provider failed to get the disk properties from the driver (unknown status, unknown health), or the provider cannot access the disk (unknown status, healthy).

### -field VDS_DS_ONLINE:1

The disk is available. The disk status value can be VDS_DS_ONLINE, even if the status of the containing pack is VDS_PS_OFFLINE.

### -field VDS_DS_NOT_READY:2

The disk is currently not ready to use. For example, if you use ACPI Power Management to request that a disk hibernate (spin down), the disk becomes temporarily unavailable.

### -field VDS_DS_NO_MEDIA:3

The disk is removable media, such as a CD-ROM drive, or contains no media.

### -field VDS_DS_FAILED:5

The disk is unavailable and cannot be used.

### -field VDS_DS_MISSING:6

No physical device is present for the disk object, even though the pack configuration information lists the disk. This status value applies to dynamic disks only.

### -field VDS_DS_OFFLINE:4

The disk is offline.

<b>Windows Vista and Windows Server 2003:  </b>This flag is not supported.

## -remarks

The <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure includes a <b>VDS_DISK_STATUS</b> value as a member to indicate the current status of a disk.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DISK_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DISK_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryunallocateddisks">IVdsService::QueryUnallocatedDisks</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_pack_status">VDS_PACK_STATUS</a>
