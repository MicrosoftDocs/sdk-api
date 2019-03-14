---
UID: NE:vds._VDS_DISK_OFFLINE_REASON
title: VDS_DISK_OFFLINE_REASON
author: windows-sdk-content
description: Defines the set of reasons for a disk to be offline.
old-location: base\vds_disk_offline_reason.htm
tech.root: VDS
ms.assetid: 45115cd5-52bb-4cb8-978b-208a2bc3c148
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDSDiskOfflineReasonCollision, VDSDiskOfflineReasonNone, VDSDiskOfflineReasonPolicy, VDSDiskOfflineReasonRedundantPath, VDSDiskOfflineReasonSnapshot, VDS_DISK_OFFLINE_REASON, VDS_DISK_OFFLINE_REASON enumeration, base.vds_disk_offline_reason, vds/VDSDiskOfflineReasonCollision, vds/VDSDiskOfflineReasonNone, vds/VDSDiskOfflineReasonPolicy, vds/VDSDiskOfflineReasonRedundantPath, vds/VDSDiskOfflineReasonSnapshot, vds/VDS_DISK_OFFLINE_REASON
ms.topic: enum
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
 - VDS_DISK_OFFLINE_REASON
product: Windows
targetos: Windows
req.typenames: VDS_DISK_OFFLINE_REASON
req.redist: 
---

# VDS_DISK_OFFLINE_REASON enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of reasons for a disk to be offline.


## -enum-fields




### -field VDSDiskOfflineReasonNone

The reason is unknown.


### -field VDSDiskOfflineReasonPolicy

The disk is offline because of the current <a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">SAN policy</a>.


### -field VDSDiskOfflineReasonRedundantPath

The disk is offline because it has a path that is the same as that of another device. This value is used when multipathing is physically enabled, but the MPIO software is not installed or is not functioning properly. (When the MPIO software is functioning properly, it exposes only one disk device.)


### -field VDSDiskOfflineReasonSnapshot

The disk is offline because it contains a volume shadow copy volume. In this case, the disk is a clone of another disk that is online.


### -field VDSDiskOfflineReasonCollision

If the disk is an MBR disk, it is offline because its disk signature is the same as that of another disk that is online. The disk signature is found in the <b>dwSignature</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structures and in the <b>Signature</b> member of the <a href="https://msdn.microsoft.com/71c361fe-8c85-4915-9776-8ad3f5837e11">DRIVE_LAYOUT_INFORMATION_MBR</a> structure.

If it is a GPT disk, it is offline for one of the following reasons:<ul>
<li>Its disk identifier is the same as that of another disk that is offline. The disk identifier is found in the <b>DiskGuid</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structures and in the <b>DiskId</b> member of the <a href="https://msdn.microsoft.com/763b0d64-6dcc-411c-aca1-3beea0890124">DRIVE_LAYOUT_INFORMATION_GPT</a> structure.</li>
<li>One of the partitions has the same partition GUID as another partition on the same disk.</li>
</ul>



### -field VDSDiskOfflineReasonResourceExhaustion


### -field VDSDiskOfflineReasonWriteFailure


### -field VDSDiskOfflineReasonDIScan


### -field VDSDiskOfflineReasonLostDataPersistence




## -see-also




<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>
 

 

