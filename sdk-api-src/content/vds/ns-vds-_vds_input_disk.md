---
UID: NS:vds._VDS_INPUT_DISK
title: "_VDS_INPUT_DISK"
author: windows-sdk-content
description: Defines the details of an input disk.
old-location: base\vds_input_disk.htm
tech.root: VDS
ms.assetid: 837981e5-8600-4add-85cf-a802615133d3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VDS_INPUT_DISK, VDS_INPUT_DISK structure [VDS], _VDS_INPUT_DISK, base.vds_input_disk, vds/_VDS_INPUT_DISK
ms.prod: windows
ms.technology: windows-sdk
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
api_name:
 - VDS_INPUT_DISK
product: Windows
targetos: Windows
req.typenames: VDS_INPUT_DISK
req.redist: 
---

# _VDS_INPUT_DISK structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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


Callers can specify a member index for all disks or use the default member index for all disks. Never mix specified and default member indexes for the disks included in the same array. Avoid using a default member index in conjunction with the <a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">IVdsVolume::Extend</a> method, unless the volume has only one plex with only one member.

The <a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>, <a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">IVdsVolume::Extend</a>, and <a href="https://msdn.microsoft.com/21c91e85-8a49-4e74-9191-37aeb03b299e">IVdsVolumePlex::Repair</a> methods pass this structure as an argument to specify disk input information.




## -see-also




<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>



<a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">IVdsVolume::Extend</a>



<a href="https://msdn.microsoft.com/21c91e85-8a49-4e74-9191-37aeb03b299e">IVdsVolumePlex::Repair</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

