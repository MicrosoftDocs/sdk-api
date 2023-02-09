---
UID: NS:vds._VDS_INPUT_DISK
title: VDS_INPUT_DISK (vds.h)
description: Defines the details of an input disk.
helpviewer_keywords: ["VDS_INPUT_DISK","VDS_INPUT_DISK structure [VDS]","base.vds_input_disk","vds/_VDS_INPUT_DISK"]
old-location: base\vds_input_disk.htm
tech.root: base
ms.assetid: 837981e5-8600-4add-85cf-a802615133d3
ms.date: 12/05/2018
ms.keywords: VDS_INPUT_DISK, VDS_INPUT_DISK structure [VDS], base.vds_input_disk, vds/_VDS_INPUT_DISK
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
req.typenames: VDS_INPUT_DISK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_INPUT_DISK
 - vds/_VDS_INPUT_DISK
 - VDS_INPUT_DISK
 - vds/VDS_INPUT_DISK
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
 - VDS_INPUT_DISK
---

# VDS_INPUT_DISK structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of an input disk.

## -struct-fields

### -field diskId

The GUID of the disk. This field is required.

### -field ullSize

Disk size in bytes. This field is required. The provider policy determines the offset, length, and number of disk extents allocated for an input disk.

### -field plexId

When extending a volume, the GUID for the plex to which the disk belongs. VDS ignores this member when creating a volume or  repairing a RAID-5 volume.


<div class="alert"><b>Note</b>  Callers can extend a volume only by extending all members of all plexes in the same operation.</div>
<div> </div>

### -field memberIdx

The member index of the disk to which the extent belongs. Either specify a <b>memberIdx</b> for all disks or specify it for none. VDS uses disks with the same <b>memberIdx</b> in the order they appear in the array. For example, the first disk in the array is always used first.


<div class="alert"><b>Note</b>  Do not specify <b>memberIdx</b> when repairing a RAID-5 volume.</div>
<div> </div>

## -remarks

A disk cannot contribute more than one plex to the same volume; however, a disk can contribute to multiple volumes.


Callers can specify a member index for all disks or use the default member index for all disks. Never mix specified and default member indexes for the disks included in the same array. Avoid using a default member index in conjunction with the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">IVdsVolume::Extend</a> method, unless the volume has only one plex with only one member.

The <a href="/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a>, <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">IVdsVolume::Extend</a>, and <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-repair">IVdsVolumePlex::Repair</a> methods pass this structure as an argument to specify disk input information.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">IVdsVolume::Extend</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-repair">IVdsVolumePlex::Repair</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>