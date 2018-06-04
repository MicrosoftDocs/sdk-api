---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VDS_DISK_STATUS enumeration


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



The <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">
        VDS_DISK_PROP</a> structure includes a <b>VDS_DISK_STATUS</b> value as a member to indicate the current status of a disk.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DISK_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DISK_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d519c3d0-7c5a-4c0c-bad9-2429490f2212">IVdsService::QueryUnallocatedDisks</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">
        VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/a83d01e6-1173-410c-b880-3bc957d3f7e9">VDS_PACK_STATUS</a>
 

 

