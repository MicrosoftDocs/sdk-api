---
UID: NE:vds._VDS_DISK_STATUS
title: VDS_DISK_STATUS (vds.h)
author: windows-sdk-content
description: Defines the set of object status values for a disk.
old-location: base\vds_disk_status.htm
tech.root: VDS
ms.assetid: 7691347d-49a6-4078-9c6c-af59a48af692
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_DISK_STATUS, VDS_DISK_STATUS enumeration [VDS], VDS_DS_FAILED, VDS_DS_MISSING, VDS_DS_NOT_READY, VDS_DS_NO_MEDIA, VDS_DS_OFFLINE, VDS_DS_ONLINE, VDS_DS_UNKNOWN, base.vds_disk_status, vds/VDS_DISK_STATUS, vds/VDS_DS_FAILED, vds/VDS_DS_MISSING, vds/VDS_DS_NOT_READY, vds/VDS_DS_NO_MEDIA, vds/VDS_DS_OFFLINE, vds/VDS_DS_ONLINE, vds/VDS_DS_UNKNOWN
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
api_name:
 - VDS_DISK_STATUS
product: Windows
targetos: Windows
req.typenames: VDS_DISK_STATUS
req.redist: 
ms.custom: 19H1
---

# VDS_DISK_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a disk.


## -enum-fields




### -field VDS_DS_UNKNOWN

The provider failed to get the disk properties from the driver (unknown status, unknown health), or the provider cannot access the disk (unknown status, healthy).


### -field VDS_DS_ONLINE

The disk is available. The disk status value can be VDS_DS_ONLINE, even if the status of the containing pack is VDS_PS_OFFLINE.


### -field VDS_DS_NOT_READY

The disk is currently not ready to use. For example, if you use ACPI Power Management to request that a disk hibernate (spin down), the disk becomes temporarily unavailable.


### -field VDS_DS_NO_MEDIA

The disk is removable media, such as a CD-ROM drive, or contains no media.


### -field VDS_DS_FAILED

The disk is unavailable and cannot be used.


### -field VDS_DS_MISSING

No physical device is present for the disk object, even though the pack configuration information lists the disk. This status value applies to dynamic disks only.


### -field VDS_DS_OFFLINE

The disk is offline.

<b>Windows Vista and Windows Server 2003:  </b>This flag is not supported.


## -remarks



The <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> structure includes a <b>VDS_DISK_STATUS</b> value as a member to indicate the current status of a disk.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DISK_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DISK_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d519c3d0-7c5a-4c0c-bad9-2429490f2212">IVdsService::QueryUnallocatedDisks</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/a83d01e6-1173-410c-b880-3bc957d3f7e9">VDS_PACK_STATUS</a>
 

 

